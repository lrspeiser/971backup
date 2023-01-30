  <div class="content">
    <div class="field field-name-body field-type-text-with-summary field-label-hidden"><div class="field-items"><div class="field-item even"><p>My notes for getting Debian Wheezy to work on the team HP laptops.</p><p>Parker did a clean install of Wheezy on Aug 15, 2014.</p><p>Here is a list of packages that I installed to get varrious things working.</p><p>apt-get install rcs subversion<br />apt-get install gnuplot gnuplot-x11<br /><span style="line-height: 1.538em;">apt-get install vim-gtk vim-gnome vim-athena</span></p><p># Installing Wireless.  I read the directions at <a href="https://wiki.debian.org/WiFi">https://wiki.debian.org/WiFi</a> and <a href="https://wiki.debian.org/iwlegacy">https://wiki.debian.org/iwlegacy</a><a href="https://wiki.debian.org/iwlegacy"> <br /></a># Add the following line to /etc/apt/sources.list<a href="https://wiki.debian.org/iwlegacy"><br /></a>deb http://http.debian.net/debian/ wheezy main contrib non-free<br /># Then run these commands and find the wireless connect menu up with the "power" icon <br /># in the upper right hand corner of the screen. <br />apt-get update &amp;&amp; apt-get install firmware-iwlwifi<br />modprobe -r iwl3945 iwlagn<br />modprobe iwl3945 ; modprobe iwlagn<br /># Check the wireless interface with<br /> iwconfig</p><p># Install packages and the gtk2 ruby gem for Parker's real time plotter.</p><p><span style="line-height: 1.538em;">apt-get install ruby rubygems ruby-mkrf ruby-dev gtk2.0-dev libgtkglext1 libgtkglext1-dev<br /></span><span style="line-height: 1.538em;">gem install gtk2</span></p></div></div></div>  </div>

  
  
</div>
  </div>
</div>
  </div>
    </div>