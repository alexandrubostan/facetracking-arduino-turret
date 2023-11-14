# Facetracking Arduino Turret

A simple turret capable of tracking your face and shooting Nerf darts at your face.

The program communicates with the Arduino using a serial connection (bear in mind that this connection was implemented using the Win32 API). The facetracking was implemented using the OpenCV C++ library.

Program was calibrated to work with [this design](https://www.littlefrenchkev.com/bluetooth-nerf-turret). Only the 3D printed body and the electrical components were used. A camera was also added (obv.).

### How to build
1. Compile *facerec.cpp* and *serial.cpp* using MSVC.
2. Upload *facerec_arduino.ino* to your Arduino.
3. Profit.

### How to use
1. Power up the contraption.
2. Connect Arduino board to the computer.
3. Launch the built executable. A window should appear on the screen.
4. If the camera captures a face, the turret should turn and follow the face.
5. Press F to shoot. Pew pew!
