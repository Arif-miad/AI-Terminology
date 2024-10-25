##

What is Projectile Motion 

Projectile motion refers to the motion of an object thrown o projected into the air under the action of gravity . Once in motion, the object, called a projectile, moves along a curved path under the influence of two forces:

1. The initial velocity imparted to the object (horizotal and vertical components)
2. The force of gravity , which acts downward.
 ##

 The Projectile montion is a classic example of two-dimensional motion becase it involves movement in both horizontal and vertical directions.

 **Componets of Projectile Motion**

 *1.Horizontal Component*

 - The horizontal motion occurs at a constant velocity becas=use there are no horizontal forces acting on the projectile (assuming air resistance is neglected).
 - The horizontal displacement at any time (t) is given by:


   $$
                             x(t) = u0x.t

   where v0x = v0cos(θ) is the horizontal component of the initial velocity v0.

   ##

   Vertical Component:

   - The vertical motion is affected by gravity, which causes the projectile to accelerate downward. This makes the vertical velocity change over time.
   - The vertical displacement at any time ( t ) is given by:


     $
                           y(t)=v 
0y
​
 ⋅t− 
2
1
​
 gt 
2


##

where
v
0
y
=
v
0
sin
⁡
(
θ
)
v 
0y
​
 =v 
0
​
 sin(θ) is the vertical component of the initial velocity, and ( g ) is the acceleration due to gravity (approximately 
9.8
,
m/s
2
)
9.8,m/s 
2
 ).

#

Resultant Path:
##
The combination of constant horizontal motion and vertically accelerated motion results in a parabolic trajectory.
The general equation for the trajectory is:
$
y
(
x
)
=
tan
⁡
(
θ
)
⋅
x
−
g
2
v
0
x
2
⋅
x
2
y(x)=tan(θ)⋅x− 
2v 
0x
2
​
 
g
​
 ⋅x 
2
 
#
Key Parameters in Projectile Motion
##
Time of Flight:
-
The total time the projectile remains in the air is called the time of flight. For a projectile launched and landing at the same height:
$
T
=
2
v
0
sin
⁡
(
θ
)
g
T= 
g
2v 
0
​
 sin(θ)
​
 #
Maximum Height:
##
The highest vertical position reached by the projectile is called the maximum height:
$
H
=
v
0
2
sin
⁡
2
(
θ
)
2
g
H= 
2g
v 
0
2
​
 sin 
2
 (θ)
​##
 
Range:
The horizontal distance the projectile travels is called the range. For a projectile launched and landing at the same height:
$
R
=
v
0
2
sin
⁡
(
2
θ
)
g
R= 
g
v 
0
2
​
 sin(2θ)
​
 ##
Conditions for Symmetrical Projectile Motion
Symmetrical motion occurs when the projectile is launched and lands at the same height. The path is symmetrical, meaning the ascent time equals the descent time.
For symmetrical motion:
The time to reach the maximum height is half of the total time of flight:

$
T
m
a
x
=
v
0
sin
⁡
(
θ
)
g
T 
max
​
 = 
g
v 
0
​
 sin(θ)
​
 
The vertical velocity at the highest point is zero:
v
y
=
0
v 
y
​
 =0
 ##
Real-Life Examples of Projectile Motion
-
A ball being thrown, kicked, or hit in sports.
-
A cannonball being fired from a cannon.
-
Water fountains, where the water follows a parabolic trajectory.
In summary, projectile motion is a type of motion that results from an initial force, where the object follows a curved path under the influence of gravity. The motion can be broken down into horizontal and vertical components, which can be analyzed independently to predict the object's path, height, time of flight, and range. By breaking down the motion into horizontal and vertical components, we can solve for various aspects of the projectile's trajectory.

```python

import math
import matplotlib.pyplot as plt

# Function to calculate the trajectory
def calculate_trajectory(v0, angle, g=9.81):
    # Convert angle to radians
    angle_rad = math.radians(angle)
    
    # Time of flight
    t_flight = 2 * v0 * math.sin(angle_rad) / g
    
    # Time intervals
    t_intervals = [i * 0.01 for i in range(int(t_flight / 0.01) + 1)]
    
    # X and Y coordinates of the projectile
    x = [v0 * math.cos(angle_rad) * t for t in t_intervals]
    y = [(v0 * math.sin(angle_rad) * t - 0.5 * g * t**2) for t in t_intervals]
    
    return x, y

# Initial velocity (m/s) and angle (degrees)
v0 = 20
angle = 45

# Calculate trajectory
x, y = calculate_trajectory(v0, angle)

# Plotting the trajectory
plt.plot(x, y)
plt.title("Projectile Motion")
plt.xlabel("Distance (m)")
plt.ylabel("Height (m)")
plt.grid(True)
plt.show()
```
![Output](https://github.com/Arif-miad/AI-Terminology/blob/main/image%20(1).png)

 
 

