

<body>
<div id="main_page" style="height:50px;border-width:0px">
</div>
<div id="main_page" style="height:1000px;width:800px;background-color:white;border-width:0px">
<div id="content_box_text">
<h1>971 CAD Download Page</h1>

<p>We are providing our robot CAD files with the hope that teams will be able to use it to
learn more about how our robots are made and then build better robots themselves.
We are asking some questions before download so we can better understand if we are achieving our
goal of helping teams by providing our CAD.
For questions or comments, please use the comments box below or 
our team <a href="contact.html">contact form</a> (select "CAD" in the "Category" drop
down menu so the correct person gets your message).
</p>

<p class="javascriptDisclamer">
<b><span class="required">This page requires javascript for form submition and download to work.  Please enable javascript.</span></b>
</p>
<script>
javascriptEnabled()
</script>

<form method="post" id="form-id" action="cgi-bin/cadDownloadRequestRB.cgi.html">
  <input id="timeOnPage" name="timeOnPage" type="hidden"/>
  <input id="eventName" name="eventName" type="hidden"/>

  <p>
    <label for="teamNumber"> <span class="required">*</span>  What is your
      <a href="http://www.usfirst.org/roboticsprograms/frc">FRC team</a> number?  <br>
    <input type="text" name="teamNumber" id="teamNumber" onchange="checkifshow()" onkeydown="checkifshow()"/></label>
    <i>(Put "N/A" (not applicable) if you don't have a team number or don't want to provide it.)</i>
  </p>

  <p>
    <label for="rookieYear"> <span class="required">*</span> 
    What was your personal rookie year in FRC?  If you started with an FRC team in 2012
    and your team started in 1989, put "2012" in the text box.  <br>
    <input type="text" name="rookieYear" id="rookieYear" onchange="checkifshow()" onkeydown="checkifshow()" /></label>
    <i>(Put "N/A" if you don't want to provide it.)</i>
  </p>

  <p>
    <label for="otherComment">    Please enter any other comments you have or 
    information you want to tell us. <i>(Optional with 250 character limit)</i>
    <br>
    <textarea name="otherComment" cols="100" rows="2" id="otherComment" 
       class="html-text-box"></textarea><br>
    </label>
  </p>

  <input type="text" name="cadYear" id="cadYear" value="" style="display:none;"/>

  <div id="showDownloads" class='show' onclick='disabledHelp(this)'>

    <!-- 2019 Season -->
    <div id="content_box" style="width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2019_Robot.png" width="100" border="0" align="left" alt="2019 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        Robot name: Tachyon<br>
        <a href="#" onclick="downloadFile('2019');">Download 2019 CAD (152 MBytes) for STEP version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2019native');">Download 2019 CAD (260 MBytes) for Native SolidWorks 2018 version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2019parts_library');">Download 2019 CAD Parts Library (309 MBytes)</a>
      </p>
      </div>
    </div>

    <!-- 2018 Season -->
    <div id="content_box" style="width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2018_Robot.png" width="100" border="0" align="left" alt="2018 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        Robot name: Curiosity<br>
        <a href="#" onclick="downloadFile('2018');">Download 2018 CAD (152 MBytes) for STEP version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2018native');">Download 2018 CAD (260 MBytes) for Native SolidWorks 2017 version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2018third');">Download 2018 CAD for Third Robot (72 MBytes)</a><br>
        More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2018Details">information and details</a> about the 2018 robot.
      </p>
      </div>
    </div>

    <!-- 2017 Season -->
    <div id="content_box" style="width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2017_Robot_100x100.jpg" width="100" border="0" align="left" alt="2017 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        Robot name: Fyn<br>
        <a href="#" onclick="downloadFile('2017');">Download 2017 CAD (277 MBytes) for STEP version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2017native');">Download 2017 CAD (438 MBytes) for Native SolidWorks 2016 version the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2017cableDriveArm');">2017 CAD for Off-Season Cable Drive Arm</a><br>
        <a href="#" onclick="downloadFile('2017singleSpeedTrans');">2017 CAD for Off-Season Single Speed Tranmission</a><br>
        <a href="#" onclick="downloadFile('2017squareDrivetrain');">2017 CAD for Off-Season Square Drivetrain with Ball Shifter Transmission</a><br>
        More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2017Details">information and details</a> about the 2017 robot.
      </p>
      </div>
    </div>

    <!-- 2016 Season -->
    <div id="content_box" style="width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2016_Robot_100x100a.jpg" width="100" border="0" align="left" alt="2016 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        <a href="#" onclick="downloadFile('2016champs');">Download 2016 CAD (242 MBytes) for the robot we took to the championship event</a><br>
        <a href="#" onclick="downloadFile('2016rev1intake');">Download 2016 CAD (45 MBytes) for revision 1 of the intake</a>.  This intake was bagged with the robot and then replaced before our first competition.<br>
        <a href="#" onclick="downloadFile('2016third');">Download 2016 CAD for Third Robot (112 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2016oct');">Download 2016 CAD for Off-Season Octagonal Drive Base (29 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2016rec');">Download 2016 CAD for Off-Season Rectangular Drive Base (42 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2016d2p2p');">Download 2016 CAD for Off-Season 2+2 Prototype Drive Base (54 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2016d2p2h');">Download 2016 CAD for Off-Season 2+2 Hybrid Drive Base (34 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2016minside');">Download 2016 CAD for Off-Season Minimized Siderail Drive Base (42 MBytes)</a><br>
        More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2016Details">information and details</a> about the 2016 robot.
      </p>
      </div>
    </div>

    <!-- 2015 Season -->
    <div id="content_box" style="height:135px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2015_Robot_100x100.jpg" width="100" border="0" align="left" alt="2015 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        Robot name: The closest we came for a name for this robot was Pandora<br>
        <a href="#" onclick="downloadFile('2015');"> Download 2015 CAD (154 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2015third');"> Download 2015 CAD for Third Robot(258 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2015oct');"> Download 2015 CAD for Octagonal Drivebase (77 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2015rec');"> Download 2015 CAD for Rectangular Drivebase (25 MBytes)</a><br>
        More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2015Details">information and details</a> about the 2015 robot.
      </p>
      </div>
    </div>

    <!-- 2014 Season -->
    <div id="content_box" style="width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2014_RobotWithBumpersAndBall_100x100.jpg" width="100" border="0" align="left" alt="2014 Robot">
      </div>
      <div id="content_box" style="width:660px">
      <p> 
        Robot name: Mammoth<br>
        <a href="#" onclick="downloadFile('2014');"> Download 2014 CAD (139 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2014c1');"> Download 2014 Offseason Configuration 1 CAD (70 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2014c2');"> Download 2014 Offseason Configuration 2 CAD (60 MBytes)</a><br>
        <a href="#" onclick="downloadFile('2014c3');"> Download 2014 Offseason Configuration 3 CAD (56 MBytes)</a><br>
        More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2014Details">information and details</a> about Mammoth
      </p>
      </div>
    </div>

    <!-- 2013 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:lt-grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2013_Robot_100x100.jpg" width="100" border="0" align="left" alt="2013 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          Robot name: Dash<br>
          <a href="#" onclick="downloadFile('2013')"> Download 2013 CAD (156 MBytes)</a><br>
          More <a class='info' onclick="noAlert(event)" href="content/team-documents.html#2013Season">information</a> about Dash
        </p>
      </div>
    </div>

    <!-- 2012 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2012_Robot_100x100.jpg" width="100" border="0" align="left" alt="2012 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          Robot name: Renegade<br>
          <a href="#" onclick="downloadFile('2012')"> Download 2012 CAD (67 MBytes)</a><br>
          More <a class="info" onclick="noAlert(event)" href="content/team-documents.html#2012Details">information and details</a> about Renegade
        </p>
      </div>
    </div>

    <!-- 2011 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2011_Robot_100x100.jpg" width="100" border="0" align="left" alt="2011 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          Robot name: Havoc<br>
          <a href="#" onclick="downloadFile('2011')"> Download 2011 CAD (69 MBytes)</a>
        </p>
      </div>
    </div>

    <!-- 2010 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2010_Robot_100x100.jpg" width="100" border="0" align="left" alt="2010 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          Robot name: Storm<br>
          <a href="#" onclick="downloadFile('2010')"> Download 2010 CAD (23 MBytes)</a>
        </p>
      </div>
    </div>

    <!-- 2009 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2009_Robot_100x100.jpg" width="100" border="0" align="left" alt="2009 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          <a href="#" onclick="downloadFile('2009')"> Download 2009 CAD (36 MBytes)</a>
        </p>
      </div>
    </div>

    <!-- 2008 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2008_Robot_100x100.jpg" width="100" border="0" align="left" alt="2008 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          <a href="#" onclick="downloadFile('2008')"> Download 2008 CAD (50 MBytes)</a>
        </p>
      </div>
    </div>

    <!-- 2007 Season -->
    <div id="content_box" style="height:115px;width:800px;border-style:solid;border-width:0px;border-color:grey;border-top-width:1px">
      <div id="content_box" style="width:100px">
        <img src="images/cadDownloadForm/2007_Robot_100x100.jpg" width="100" border="0" align="left" alt="2007 Robot">
      </div>
      <div id="content_box" style="width:660px">
        <p> 
          <a href="#" onclick="downloadFile('2007')"> Download 2007 CAD (55 MBytes)</a>
        </p>
      </div>
    </div>
  </div>
</form>

<hr>
<h2>CAD Links for other teams</h2>
<ul>
  <li><a href="http://www.greybots.com/cad.html">973 - The Greybots</a></li>
  <li><a href="http://www.simbotics.org/resources/cad">1114 - Simbotics</a></li>
  </li>
</ul>
<p>
    Please send us any additional links or changes by using our 
    <a href="contact.html">team contact from</a> (select "CAD" in the "Category" drop
    down menu so the correct person gets your message). 
<p>
</div>

<!-- Parker added checkifshow() at the end to make the page show the links when the browser back button is hit.-->
<script>checkifshow();</script>

</body></html>
</div></div></div>  </div>

  
  
</div>
  </div>
</div>
  </div>
    </div>
    
    </div></div>