  
  
  <div class="content">
    <div class="field field-name-body field-type-text-with-summary field-label-hidden"><div class="field-items"><div class="field-item even"><h2>Notes on 971 Programming concepts and implementation</h2>
 

<h3>Comments about the 2010 drive performance from Jim Bathgate, a mentor for the Notre Dame team (Oct 27, 2010)</h3>

<div style="margin-left: 20px; margin-right: 20px;"><p><i>Notre Dame was very impressed with the speed and smoothness of the driver on the Mountain View robot.  Of course a significant part of that is the skill of the driver himself, but I noticed they used a steering wheel on the driver interface and it seemed as if the driver was as good in reverse as he was in the forward direction.  I wondered if they used a switch keyed to their software that allowed driving in reverse as if they were driving in forward direction.  In fact their robot had the ball capture rollers at both ends to allow scoring from either end and it didn’t seem to matter to the driver which end of the robot he used to score.</i></p></div>

<h3>Austin wrote back with this description of the drive code architecture</h3>

<div style="margin-left: 20px; margin-right: 20px;">
<p>We've been building off what 254 did a couple years ago for their
drivetrain controls, and it's working nicely.</p>

<p><b>Steering Wheel:</b><br />
We like the steering wheel and throttle sticks because it
separates the controls.  When a driver is driving, they typically
don't want the steering to move when they are changing the throttle,
and the same for not wanting the throttle to move when they are
changing the steering.  By putting those on separate hands, that makes
it really easy to separate the action of steering from the action of
throttle.  I like to think it in terms of orthogonality.  You want the
inputs that have distinct meanings to have distinct orthogonal results
in the driving of the robot.</p>

<p><b>Car Steering:</b><br />
Along the same lines, we implement software car steering.  If a
driver is trying to drive a 5 foot diameter circle, and wants to go
faster, the drive would like to just increase the throttle, and not
have to mess with steering as well.  Same goes for when the driver has
a good velocity picked out and wants to turn.  I view this as another
case where we want orthogonality in how the inputs respond.
Unfortunately, car steering won't let you spin in place, so we have a
button called "quickturn" that we hit in order to revert back to
simple mixed controls, which lets us turn in place.  This button isn't
used very often in practice.  We modify the principle of car steering
by having it always turn the same way if you are going forwards or
backwards, which makes it so that forwards and backwards are almost
interchangeable.  The driver just pulls the throttle stick backwards,
and the robot drives exactly the same as it did before, except
backwards.</p>

<p><b>Negative Inertia:</b><br />
Another thing that you will find is that the robot will feel
"sluggish" when turning or accelerating.  You turn the wheel, and it
takes a little bit to accelerate up to the correct angular velocity.
We solve that by the same way that the IBM trackpoint does.  We add
the velocity of the stick in question to the angle of the stick, and
use that.  This makes it so that if the driver is cranking the wheel
to the left quickly to make a turn, the bot will interpret that action
like the driver is starting to try to turn quickly, and add more turn
power to try to anticipate that action.</p>

<p><b>Linearization of victors:</b><br />
The victors on the drivetrain aren't very linear at all, so we
propped the bot up on blocks, and plotted input power vs output speed,
and best fitted a 7th order polynomial to make the victors act more
linear.  This helps a lot with slow movement.</p>

<p>The basic algorithm for steering is as follows.  We have some extra
code that deals with full power to take the extra power above 1 and
put some of that into negative power on the other motor, and some more
code to add in the negative inertia.</p>
<pre>
if quickturn:
   left.linearized_power(throttle.y() + wheel.x())
   right.linearized_power(throttle.y() - wheel.x())
else:
   left.linearized_power(throttle.y() + abs(throttle.y()) * wheel.x())
   right.linearized_power(throttle.y() - abs(throttle.y()) * wheel.x())
</pre>
</div>

</div></div></div>  </div>

  
  
</div>
  </div>
</div>
  </div>
    </div>