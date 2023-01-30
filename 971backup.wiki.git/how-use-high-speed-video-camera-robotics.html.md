     
  
  <div class="content">
    <div class="field field-name-body field-type-text-with-summary field-label-hidden"><div class="field-items"><div class="field-item even"><p align="right"><i>Jerry Morrison (FIRST Team 971) and Ron Crane (FIRST Team 670)</i></p>

<p>A high speed video camera is very useful for testing, measuring, calibrating, and debugging robot mechanisms. It's like an oscilloscope for mechanical engineers.

<h2>Equipment needed</h2>
<ul>
<li> A high speed video camera like the <a href="http://www.casio-intl.com/asia-mea/en/dc/ex_zr200/spec/">Casio Exilim EX-ZR200</a>. (It can record video at 30, 120, 240, 480, and 1000 fps.)
<li> Bright light.
<li> (No tripod needed. These are fast shutter times.)
</ul>

<p>Let's start with some examples from the FRC 2013 season ("Ultimate Ascent").

<p>Frisbee launch and flight from a circular shooter prototype (120 fps):
<a href="http://www.youtube.com/embed/myBpNC7xg84?rel=0">Circular Shooter Flight 24</a>
<br>

<!--break-->

<p>Measuring a circular shooter prototype (1000 fps):
<a href="http://www.youtube.com/embed/Q6OMCkT2XNw?rel=0">Circular Shooter Flight 21</a><br>

<p>Measuring a two-stage linear shooter prototype (1000 fps):
<a href="http://www.youtube.com/embed/G2vnKWs_a6Q?rel=0">Linear Shooter Test 5</a><br>

<p>By single-stepping through this 1000 fps video, you can measure how fast the Frisbee moves. (The lines on the backboard are 1" apart and the frames are 1 msec apart.)

<p>You can also measure the rotational speeds of the wheels before and after they push the Frisbee, and the rotational speed of the Frisbee on exit, and compute the slippage.

<h2>Best Practices</h2>
<ul>
<li> Put high-contrast markers on the wheels, e.g. aluminum duct tape that reflects the light source, to measure their rotational speeds.
<li> Put high-contrast ruler marks on the surface behind the Frisbee to measure its linear speed. (1" spacing in these videos.)
<li> Put high-contrast marks on the Frisbee, e.g. draw a diameter line with a paint pen, to measure its rotational speed.
<li> Frame a tight shot (just enough visual context) since the camera records smaller images at higher frame rates.
<li> Record each test run to a separate video file.
<li> Announce a 3-2-1 countdown to coordinate starting the test run.
<li> In each test run, the interesting part will be surrounded by a lot of playback waiting time. So trim it in-camera. This camera does a great job of trimming.
<li> To measure speed, single-step through the video in camera, in the QuickTime movie player, or in Windows Movie Maker. Measure distance using reference lines or the game pieces (see below). Measure time by counting frames. Then compute speed = distance / time.
</ul>

<h2>Check Quality</h2>
<p>Here we are, checking the Frisbee liftoff from a circular shooter prototype (480 fps):
<a href="http://www.youtube.com/embed/eH-YYHz0OGo?rel=0">Circular Shooter Liftoff Test 21</a>
<br>

<p>That's a nice, level liftoff. In comparison, the Frisbees wobbled terribly coming off our linear shooter prototype:
<a href="http://www.youtube.com/embed/sLn2lnzDiQA?rel=0">3 Linear Shooter Liftoff Tests</a>
<br>

<p>That may be because the Frisbee expands after being squeezed between the tire and the fence.

<p>If the angle of observation is not 90 degrees to the direction of travel, then divide the distance observed by the sine of the angle. This works for round objects like balls and Frisbees viewed from edge. A long thin object like an arrow would need almost no correction factor.

<h2>Measure Flying Speed</h2>
<p>We can use the Frisbee itself to measure flying distances, then compute speed. These Frisbees are about 10.9-11" in diameter. Hold a paper or clear plastic edge against the screen, then count the number of frames between the Frisbee's leading edge to its trailing edge crossing that reference line.

<pre>
    d = length of the object along the travel line (leading edge to trailing edge)
    fc = frame count to cross the reference line
    fps = frames per second video frame rate

    speed = d * fps / fc
</pre><p>

<h2>Measure Mechanism Speed</h2>
<p>Our Frisbee intake and hopper are designed to pick up two side-by-side Frisbees then rapidly queue and pass them on to the shooter mechanism. It avoids jamming by keeping the Frisbees from contacting each other in the hopper:

<a href="http://www.youtube.com/embed/-ymu2DEwGHc?rel=0">3 Helical Frisbee Hopper Test</a>
<br>

<p>At 120 fps recording and 30 fps playback, you get a 4x slow motion view of the mechanism in action. So divide the 4 second playback time by 4 to compute how long it takes for a Frisbee to enter the mechanism and get through the hopper.

<h2>Compare Designs</h2>
<p>Here, we're testing ideas for blocking Frisbees: <a href="http://www.youtube.com/embed/0hRpuQmpI_4?rel=0">Frisbee Blocker Test</a>
<br></div></div>

</div>
  </div>
</div>
  </div>
    </div>