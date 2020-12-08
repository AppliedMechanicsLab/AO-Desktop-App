# AO-Algorithm-App


## Acceleration Data File format

* Each file contains the acceleration measurement of one accelerometer
* Format: n*4 matrix
* Units: Meter, Second, Kg

| Time | Acc_x | Acc_y | Acc_z |
|------|-------|-------|-------|
| ...  | ...   | ...   | ...   |
| ...  | ...   | ...   | ...   |
 

## Position and direction of accelerometers
* X1={0,0,0.83}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X2={0,0.1,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X3={0.15,0,0.75}, N={{1, 0, 0}, {0, 1, 0}, {0, 0, 1}}
* X4={-0.15,0,0.75}, N={{0, 1, 0}, {-1, 0, 0}, {0, 0, 1}}

X5={0,0,0.67} 


## Initial condition
* R = I
* The position of the center of mass Xcm of the ellipsoid is (0,0,0.75)
* The initial velocity of Xcm is (0.75,0,0)
* The angular velocity of the body is (5,5,5)
