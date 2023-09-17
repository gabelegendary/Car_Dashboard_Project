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
Introduction:

Welcome to the gabelegendary/Car_Dashboard_Project repository! This repository hosts the source code and documentation for an innovative and versatile client-server application designed to meet a variety of communication needs. Whether you're working with TCP/IP, Serial, or CAN protocols, this project provides a seamless solution for real-time data exchange.

This project boasts an intuitive graphical user interface (GUI) built with Qt, making it suitable for cross-platform use. From monitoring vehicle speed to tracking temperature and battery levels, this system ensures you have all the essential information at your fingertips. It even handles lighting signals effortlessly, simplifying your control tasks.

I'll guide you through the architecture, tools, technologies, and challenges we faced during development, giving you valuable insights into the project's inner workings.

Feel free to explore the code, contribute to its improvement, and adapt it to your specific requirements. Thank you for visiting this repository, and I hope you find our project valuable for your needs!

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

# Tools and Technologies Employed:

- **Version Control System / Continuous Integration**: Git and GitHub were utilized to monitor changes and facilitate collaboration throughout the software development process.

- **GUI Design and Sound Implementation**: Qt, a versatile cross-platform application framework, was chosen for creating graphical user interfaces and incorporating sound elements.

- **Project Configuration, Dependency Management, Builds**: CMake was employed to efficiently manage the build process for software projects. Visual Studio Code (VSC) served as the code editor for writing and debugging code. PlatformIO, an open-source ecosystem, was harnessed to streamline cross-platform development in embedded systems, simplifying project management for microcontrollers.

# Project-Architecture
![image](https://github.com/gabelegendary/Car_Dashboard_Project/assets/109476146/7fefb876-0178-448d-bef2-1ad9e540794f)

# Challenges Faced:

- Technical Compatibility Challenges: Dealing with team members using diverse operating systems (Linux, Windows, macOS) introduced compatibility issues, particularly concerning synchronization of sound, graphical user interface (GUI), and port configurations.

- Testing Complexities: Ensuring the functionality of all components, especially within the context of Controller Area Network (CAN) communication, proved to be a complex task. CAN communication, with its support for multi-master setups and message-based protocols, posed unique testing challenges.

- Quality Assurance: Maintaining consistent code quality and guarding against regressions became challenging due to frequent updates from various team members. To address this, we implemented a form of continuous integration to prevent conflicts and uphold code quality standards.

- Learning Curve: The learning curve associated with adopting new tools, frameworks (such as Qt), and unfamiliar technologies during the project was time-intensive and temporarily impacted the pace of development.

# Contributors
- GabeLegendary
- HomajonB
- nkkyviv
- Vishnugundu
- mhistamartins

To compile and execute both the client and server applications on the desktop, follow these steps:

1. Create a new directory and navigate into it:
   ```
   mkdir build && cd build
   ```

2. Configure the project using CMake, build it with 'make,' and run the server and client applications:
   ```
   cmake .. && make && ./server & ./client
   ```

**Note**: The default communication protocol utilized here is TCP (for network communication). If you wish to switch to the UART communication protocol, modify the 'CMakeLists.txt' file at line 7 as follows:

```cmake
set(USE_UART ON) #Change the ON to OFF
```

This will enable the UART communication protocol for your project.
