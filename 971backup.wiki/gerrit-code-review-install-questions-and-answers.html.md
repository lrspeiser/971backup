  
  <div class="content">
    <div class="field field-name-body field-type-text-with-summary field-label-hidden"><div class="field-items"><div class="field-item even"><p><a href="mailto:root@robotics">root@robotics</a>:/seagate/tmp/gerrit_debian_package# dpkg -i gerrit_2.9_all.deb<br />
(Reading database ... 51056 files and directories currently installed.)<br />
Preparing to replace gerrit 2.9 (using gerrit_2.9_all.deb) ...<br />
[ ok ] Stopping Gerrit Code Review: gerrit.<br />
usermod: no changes<br />
Unpacking replacement gerrit ...<br />
Setting up gerrit (2.9) ...<br />
[....] Starting Gerrit Code Review : gerrit<br />
No Gerrit site found. Will Initialize Gerrit first...</p>
<p>*** Gerrit Code Review 2.9<br />
*** </p>
<p>Create &#039;/var/lib/gerrit/review_site&#039; [Y/n]? Y</p>
<p>*** Git Repositories<br />
*** </p>
<p>Location of Git repositories   [git]: </p>
<p>*** SQL Database<br />
*** </p>
<p>Database server type           [h2]: </p>
<p>*** Index<br />
*** </p>
<p>Type                           [LUCENE/?]: </p>
<p>*** User Authentication<br />
*** </p>
<p>Authentication method          [OPENID/?]: HTTP<br />
Get username from custom HTTP header [y/N]?<br />
SSO logout URL                 : </p>
<p>*** Review Labels<br />
*** </p>
<p>Install Verified label         [y/N]? </p>
<p>*** Email Delivery<br />
*** </p>
<p>SMTP server hostname           [localhost]:<br />
SMTP server port               [(default)]:<br />
SMTP encryption                [NONE/?]:<br />
SMTP username                  : </p>
<p>*** Container Process<br />
*** </p>
<p>Run as                         [gerrit]:<br />
Java runtime                   [/usr/lib/jvm/java-7-openjdk-i386/jre]:<br />
Copy gerrit.war to /var/lib/gerrit/review_site/bin/gerrit.war [Y/n]?<br />
Copying gerrit.war to /var/lib/gerrit/review_site/bin/gerrit.war</p>
<p>*** SSH Daemon<br />
*** </p>
<p>Listen on address              [*]:<br />
Listen on port                 [29418]: </p>
<p>Gerrit Code Review is not shipped with Bouncy Castle Crypto SSL v149<br />
  If available, Gerrit can take advantage of features<br />
  in the library, but will also function without it.<br />
Download and install it now [Y/n]?<br />
Downloading <a href="http://www.bouncycastle.org/download/bcpkix-jdk15on-149.jar">http://www.bouncycastle.org/download/bcpkix-jdk15on-149.jar</a> ... OK<br />
Checksum bcpkix-jdk15on-149.jar OK</p>
<p>Gerrit Code Review is not shipped with Bouncy Castle Crypto Provider v149<br />
** This library is required by Bouncy Castle Crypto SSL v149. **<br />
Download and install it now [Y/n]?<br />
Downloading <a href="http://www.bouncycastle.org/download/bcprov-jdk15on-149.jar">http://www.bouncycastle.org/download/bcprov-jdk15on-149.jar</a> ... OK<br />
Checksum bcprov-jdk15on-149.jar OK<br />
Generating SSH host key ... rsa... dsa... done</p>
<p>*** HTTP Daemon<br />
*** </p>
<p>Behind reverse proxy           [y/N]? y<br />
Proxy uses SSL (https://)      [y/N]? y<br />
Subdirectory on proxy server   [/]: /gerrit/<br />
Listen on address              [*]: localhost<br />
Listen on port                 [8081]:<br />
Canonical URL                  [<a href="https://localhost/gerrit/%5D:">https://localhost/gerrit/]:</a> <a href="https://robotics.mvla.net/gerrit/">https://robotics.mvla.net/gerrit/</a></p>
<p>*** Plugins<br />
*** </p>
<p>Install plugin commit-message-length-validator version v2.9 [y/N]? y<br />
Install plugin download-commands version v2.9 [y/N]? y<br />
Install plugin replication version v2.9 [y/N]?<br />
Install plugin reviewnotes version v2.9 [y/N]?<br />
Install plugin singleusergroup version v2.9 [y/N]? y</p>
<p>Initialized /var/lib/gerrit/review_site<br />
Executing /var/lib/gerrit/review_site/bin/gerrit.sh start<br />
Starting Gerrit Code Review: OK</p>
</div></div></div>  </div>

  
  
</div>
  </div>
</div>
  </div>
    </div>