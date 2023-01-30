<div class="content">
    <div class="field field-name-body field-type-text-with-summary field-label-hidden"><div class="field-items"><div class="field-item even"><h2>Apache Configuration Notes</h2><p>cd /etc/apache2/<br /><span style="line-height: 1.538em;">sudo a2enmod headers<br /></span><span style="line-height: 1.538em;">sudo a2enmod proxy<br /></span><span style="line-height: 1.538em;">sudo a2enmod proxy_http<br /></span><span style="line-height: 1.538em;">sudo a2enmod rewrite<br /></span><span style="line-height: 1.538em;">sudo /etc/init.d/apache2 restart<br /></span><span style="line-height: 1.538em;">cd sites-available/</span></p><p># October 10, 2014: I figured out how to use the "RedirectPermanent" command in Apache to tell the world to use a different URL.  This worked well.  Michael<br /># <a href="http://httpd.apache.org/docs/current/mod/mod_alias.html#redirectpermanent">http://httpd.apache.org/docs/current/mod/mod_alias.html#redirectpermanent</a> </p><p><span style="line-height: 1.538em;">cat &gt; losaltosrobotics  &lt;&lt; EOF</span></p><pre style="padding-left: 30px;"># From <a href="http://docs.plone.org/manage/deploying/front-end/apache.html">http://docs.plone.org/manage/deploying/front-end/apache.html</a>

UseCanonicalName On

&lt;VirtualHost *:80&gt;
    ServerName losaltosrobotics.schuhusa.com
    ServerAlias losaltosrobotics.schuhusa.com
    # Tell the world to use losaltosrobotics.org instead.  The is a permanent redirect.
    RedirectPermanent / http://losaltosrobotics.org/
&lt;/VirtualHost&gt;

&lt;VirtualHost *:80&gt;
    ServerName www.losaltosrobotics.org
    ServerAlias www.losaltosrobtics.org
    # Tell the world to use losaltosrobotics.org instead.  The is a permanent redirect.
    RedirectPermanent / http://losaltosrobotics.org/
&lt;/VirtualHost&gt;


#NameVirtualHost *
&lt;VirtualHost *:80&gt;
    ServerName losaltosrobotics.org
    ServerAlias losaltosrobotics.org losaltosrobotics.schuhusa.com www.losaltosrobotics.org
    ServerSignature On

    Header set X-Frame-Options "SAMEORIGIN"
    Header set Strict-Transport-Security "max-age=15768000; includeSubDomains"
    Header set X-XSS-Protection "1; mode=block"
    Header set X-Content-Type-Options "nosniff"
    Header set Content-Security-Policy-Report-Only "default-src 'self'; img-src *; style-src 'unsafe-inline'; script-src 'unsafe-inline' 'unsafe-eval'"

    ProxyVia On

    # prevent your web server from being used as global HTTP proxy
    &lt;LocationMatch "^[^/]"&gt;
      Deny from all
    &lt;/LocationMatch&gt;

    &lt;Proxy *&gt;
        Order deny,allow
        Allow from all
    &lt;/Proxy&gt;

    # This turns on the Apache rewrite module.  <a href="http://httpd.apache.org/docs/current/rewrite/">http://httpd.apache.org/docs/current/rewrite/</a>
    RewriteEngine on
    # The RewriteRule "^/(.*)" sends matches on all paths to the $1.  The "P" flag says to use 
    # the "Proxy" module <a href="http://httpd.apache.org/docs/current/rewrite/flags.html#flag_p">http://httpd.apache.org/docs/current/rewrite/flags.html#flag_p</a>
    # The "L" says that is the last rule to be processed <a href="http://httpd.apache.org/docs/current/rewrite/flags.html#flag_l">http://httpd.apache.org/docs/current/rewrite/flags.html#flag_l</a>
    # The VirtualHostBase and other text is interpreted by Zope onwhich Plone runs.  <a href="http://docs.zope.org/zope2/zope2book/VirtualHosting.html">http://docs.zope.org/zope2/zope2book/VirtualHosting.html</a>
    RewriteRule ^/(.*) http://localhost:8080/VirtualHostBase/http/losaltosrobotics.org:80/Main/VirtualHostRoot/$1 [P,L]

&lt;/VirtualHost&gt;
</pre><div>EOF</div><p>pd ..<br /><span style="line-height: 1.538em;">a2ensite losaltosrobotics # Tell apache to use the losaltosrobotics configuration file.<br /></span><span style="line-height: 1.538em;">service apache2 reload    # Restart the server</span></p><p><span style="line-height: 1.538em;">Now, both <a href="http://LosAltosRobotics.org">LosAltosRobotics.org</a> and <a href="http://LosAltosRobotics.org:8080/Main">LosAltosRobotics.org:8080/Main</a> work.</span></p><div>Michael</div><div></div><div>Back to the main <a href="robotics-server.html">Robotics Server Page</a>.</div></div></div></div>  </div>

  
  
</div>
  </div>
</div>
  </div>
    </div>