# Rope-Delivery-Robot Summary
Developed for a college-wide robotics competition to create an autonomous seed-delivery robot, demonstrating a practical application of robotics for streamlined sample planting, resulting in a first place competition victory

https://github.com/user-attachments/assets/61437b79-7de4-49bb-a286-b65e70ba0256

# Full-Description
This project started out as assigned work for my engineering class, although I did have
two entries into the competition as I was attending two classes that were competing. The
goal of this project was to make an autonomous robot that could deliver “seeds”
(golfballs) on to targets that were a designated horizontal distance along the rope. For
this we were given certain information that we could use on the robot, that being, the
total rope length, the horizontal distance of the targets, and the total sag of the rope. For
one of my entries, I decided I wanted to attempt a fully autonomous system that could
work on a rope of any length or sag, while only requiring the horizontal distance of
targets from the user.
This was done with a specific method that I had devised. In the nature of saving time, I
will try to simplify the process as much as possible. The robot used pressure sensors to
measure specifically the change in pressure over time, which could then be used to find
the middle of the rope. The robot also had a quadrature encoder which could measure
the total distance traveled by the robot. The robot would then define the length travelled
to reach the middle of the rope. After this was done, the robot would head back to the
start and measure the total sag of the rope. Lastly the robot would convert the start
height and distance, and the middle height and distance into points on a cartesian plane,
and then it would create a third point by mirroring the rope across the axis at the middle
point. The robot could then use these three points to estimate a parabolic function that
followed the rope's path (it could not be catenary as the catenary function doesn’t
account for the robot’s weight). Lastly, the robot could use this function to make another
function for horizontal distance traveled based on arc length that the robot could then
use to find the location of the targets.
