#DJI Onboard SDK ROS (3.2) Packages
## We modified this package based on DJI Onboard SDK ROS (3.2) in ways that
1. Increasing Baudrate from 230400 to 921600 bps in order to cope with increasted IMU publishing and sending virtual command rates (100Hz). (They were 50Hz).
2. Directly sending a control command (roll, pitch angles, yaw rate and vertical velocity) via serial port to N1 autopilot (original DJI M100 autopilot) in order to avoid using ROS service call for this.
3. Publishing IMU and odomtery message topics (using ROS topic) using [ROS standard coordinate system](http://www.ros.org/reps/rep-0103.html) and [this](http://www.ros.org/reps/rep-0105.html).
4. Fixing some buffer overflow error.
5. Some extra features such as deadzone recovery and auto-trim compensation. 

####Please refer to <https://developer.dji.com/onboard-sdk/documentation/github-platform-docs/ROS/README.html> in DJI Developer Website.