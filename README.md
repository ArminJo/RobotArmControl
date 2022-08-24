<div align = center>

# RobotArmControl a MeArm V0.4 robot control library
Program for controlling a [robot arm with 4 servos](https://www.instructables.com/id/4-DOF-Mechanical-Arm-Robot-Controlled-by-Arduino) using 4 potentiometers and/or an IR Remote.

[![Badge License: GPLv3](https://img.shields.io/badge/License-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)
 &nbsp; &nbsp; 
[![Badge Version](https://img.shields.io/github/v/release/ArminJo/RobotArmControl?include_prereleases&color=yellow&logo=DocuSign&logoColor=white)](https://github.com/ServoEasing/RobotArmControl/releases/latest)
 &nbsp; &nbsp; 
[![Badge Commits since latest](https://img.shields.io/github/commits-since/ArminJo/RobotArmControl/latest?color=yellow)](https://github.com/ArminJo/RobotArmControl/commits/master)
 &nbsp; &nbsp; 
[![Badge Build Status](https://github.com/ArminJo/RobotArmControl/workflows/TestCompile/badge.svg)](https://github.com/ArminJo/RobotArmControl/actions)
 &nbsp; &nbsp; 
![Badge Hit Counter](https://visitor-badge.laobi.icu/badge?page_id=ArminJo_RobotArmControl)
<br/>
<br/>
[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://stand-with-ukraine.pp.ua)

Smooth servo movements are controlled by the [Servo easing library for Arduino](https://github.com/ArminJo/ServoEasing).<br/>
Used in the "RobotArmControl" example of Arduino library [ServoEasing](https://github.com/ArminJo/ServoEasing/tree/master/examples/RobotArmControl).

</div>

<br/>

| RobotArm | Control board | Instructable |
|-|-|-|
| ![RobotArm](pictures/RobotArmBlack.jpg) | ![Control board](pictures/RobotArmControlBoard.jpg) | [![Instructable](https://github.com/ArminJo/Arduino-OpenWindowAlarm/blob/master/pictures/instructables-logo-v2.png)](https://www.instructables.com/id/4-DOF-Mechanical-Arm-Robot-Controlled-by-Arduino) |

<br/>

# Calibration
To calibrate your robot arm, open the Serial Monitor, move the arm manually and change the microsecond values for the `PIVOT_MICROS_AT_*`, `LIFT_MICROS_AT_*`, `HORIZONTAL_MICROS_AT_*` and `CLAW_MICROS_AT_*` positions in *RobotArmServoConfiguration.h*.

The example uses the `EASE_USER_DIRECT` easing type for all servos except the claw to implement **movements by inverse kinematics**.

<br/>

# Compile options / macros for this software
To customize the software to different requirements, there are some compile options / macros available.<br/>
Modify them by enabling / disabling them, or change the values if applicable.

| Name | Default value |Description |
|-|-|-|
| `ROBOT_ARM_HAS_IR_CONTROL` | disabled | IR remote control is enabled. |
| `ROBOT_ARM_HAS_RTC_CONTROL` | disabled | A DS3231 is attached to the control. |

