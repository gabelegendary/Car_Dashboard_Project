# Table of Contents
1. Introduction
2. Requirements
3. Project Overview
4. Tools and Technologies
5. Project Architecture
6. Challenges
7. Contributors
8. Building the project

# Introduction
Welcome to Dashboard_Pro v1.0, a collaborative endeavor led by me and my exceptional team. Join us on this exciting journey as we unveil our innovative creation, a testament to our technical prowess, creativity, problem-solving abilities, and unwavering dedication. We invite you to delve into the world where technology and teamwork converge, powering the realization of this remarkable project. Prepare for an exhilarating experience!

# Requirements
- The client and the server shall not depend on a specific communication protocol.
- They shall be able to communicate to each other using TCP/IP and Serial & CAN protocols
- Max. speed is 240 km/h
- Temperature is in the range of [-60, 60] °C
- Battery level in percent.

# On the server GUI, there is a:
- A slider for speed. Speed is an integer in the range of 0 and 240.
- A slider for temperature. Temperature is an integer in the range of -60 and 60
- A slider for battery level. Battery level is an integer in the range of 0 and 100.
- Three checkboxes for the light signals:
- When left is checked, right shall be disabled and when right is checked, left shall be disabled.
- When warning is checked both the left.right checkboxes shall be disabled.
- When none of the checkboxes is checked, all of them shall be enabled

# On the client GUI there is a:
Simple dashboard to showcase real-time data, including speed, temperature, battery level, lighting signals, and the status of communication. Additionally, ensure it promptly alerts any communication problems between the client and server.

# Project-overview
![image](https://github.com/gabelegendary/Car_Dashboard_Project/assets/109476146/728ad4d3-1e2a-4abb-9a65-3870fb0f7238)

