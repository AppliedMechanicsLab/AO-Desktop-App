1) Data format

*Each file contains the acceleration measurement of one accelerometer
*Format: n*4 matrix

Time Acc_x Acc_y Acc_z

2) No noise

3) Time=1.5s Frequency=4000Hz

4)Acc5 records the acceleration of point 5 in global configuration;Acc1 to Acc4 records the components of the acceleration of Acc corresponding to its material axes

5) Units: Meter, Second, Kg

5) Position and direction of accelerometers
X1={0,0,0.83}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
X2={0,0.1,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
X3={0.15,0,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
X4={-0.15,0,0.75}, N={{0, 1, 0}, {-1, 0, 0}, {0, 0, 1}}

X5={0,0,0.67}, N={{0, 0, -1}, {0, 1, 0}, {1, 0, 0}} For check

6)Geometry of rigid body
Ellipsoid (a=0.15, b=0.1, c=0.08)

7)Initial condition
*R=I
*The position of the center of mass Xcm of the ellipsoid is (0,0,0.75)
*The initial velocity of Xcm is (0.75,0,0)
*The angular velocity of the body is (5,5,5)
