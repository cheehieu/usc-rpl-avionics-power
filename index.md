---
layout: project
title: usc-rpl-avionics-power
subtitle: A power distribution system for avionics equipment on a hybrid-powered rocket.
---

<img src="http://niftyhedgehog.com/usc-rpl-avionics-power/images/power_3d_profile.jpg">

## Overview
The USC Rocket Propulsion Lab's "Traveler" rocket contained several embedded electronics for logging flight data and communicating with a ground station. When I first joined the team, each of these systems had their own battery packs (mostly AA's in series). With my battery experience working on lithium polymer packs for an AUV, I designed a central power distribution system to power the rocket's on-board avionics equipment.

The hybrid-powered rocket was designed to reach outer space, with a mission apogee just beyond the 100km Karman line. This feat had never been achieved by a student team before, so we had to plan for things going awry. We usually operate in middle of the Balls, California desert and there is risk of the rocket landing several miles from the launch site. Therefore, the GPS tracking system must be reliable in the event of a multi-day recovery recon, especially if communications are lost.


## Hardware
The major avionics components in the rocket were the Arduino, Byonics, Raven, and BigRedBee embedded systems. The [Arduino](http://www.arduino.cc/en/Main/ArduinoBoardMega2560) is a sensor-rich microcontroller platform with pressure transducer, accelerometer, gyroscope, Xbee radio, and Garmin GPS. The [Byonics](http://www.byonics.com/) is a GPS tracker that can transmit and receive analog and digital telemetry. The [Raven](http://www.featherweightaltimeters.com/The_Raven.php) Altimeter is a flight-logging platform with axial/lateral accelerometer, barometer, temperature, and flight counter. The [BigRedBee](http://www.bigredbee.com/blgps_2mhp.htm) is a portable integrated GPS/APRS transmitter with GPS receiver, which can record waypoints.

<img src="http://niftyhedgehog.com/usc-rpl-avionics-power/images/power_2d.jpg" width="50%">
<img src="http://niftyhedgehog.com/usc-rpl-avionics-power/images/power_3d_top.jpg" width="49%">

My initial plan was to pack in as much battery power that could fit in the 4" diameter rocket hull. After analyzing the power requirements for all systems and reviewing the budget requiremnets, I decided on using three 2-cell LiPo batteries in parallel to power the Arduino, BigRedBee, and Raven avionics systems. One 3-cell LiPo battery would power the Byonics GPS. This should be enough battery power to run all of the components simultaneously for several hours. And if my calculations are correct, the Byonics GPS will run for 6 days in the worst-case scenario that we are unable to track the rocket to landing.

The LiPo battery cells and switching voltage regulators are an efficient solution for a redundant fault-tolerant power distribution system. The rocket already has redundant data-logging sensors and GPS transmitters. So, by configuring 3 cells in parallel, the current capacity (runtime) increases and also introduces redundancy; if one battery pack fails, the avionics can still run on the other two. I also selected polarized snap-in Molex connectors to maintain robust connections to combat the large vibrations and G-forces encountered during flight.


## 3D
<iframe width="640" height="480" src="https://sketchfab.com/models/a31195d64f7740e985684c9ff884b9ec/embed" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" onmousewheel=""></iframe>

<p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;">
    <a href="https://sketchfab.com/models/a31195d64f7740e985684c9ff884b9ec?utm_source=oembed&utm_medium=embed&utm_campaign=a31195d64f7740e985684c9ff884b9ec" target="_blank" style="font-weight: bold; color: #1CAAD9;">Avionics Power PCB</a>
    by <a href="https://sketchfab.com/hieu?utm_source=oembed&utm_medium=embed&utm_campaign=a31195d64f7740e985684c9ff884b9ec" target="_blank" style="font-weight: bold; color: #1CAAD9;">hieu</a>
    on <a href="https://sketchfab.com?utm_source=oembed&utm_medium=embed&utm_campaign=a31195d64f7740e985684c9ff884b9ec" target="_blank" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a>
</p>
