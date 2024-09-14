---
title: "Rivian Internship"
description: "Made an Arduino module that injects CAN signals to simulate brakes being pressed on a lighting rig. Created a python software that automated the creation of test cases in Jama."
dateRange: "May 2023 - August 2023"
pubDate: "May 2023"
heroImage: "/RivianCar.png"
badge: "Professional Experience"
tags: ["CAN Protocol","Arduino / C++", "Python","CANalyzer"]
---

Interning at Rivian under the Body Engineering team was a great interdisciplinary experience. I took on challenging projects that focused more on the intersection of mechanical and electrical design and learned new concepts and skills like CAN protocol and C++ / Python.

<h3>Lighting Rig Project</h3>

The lighting rig is a setup of all the lighting and electrical hardware components for a Rivian car. It's typically used for performing tests and verifying software and hardware changes. For many tests, the brake lights need to be activated as a prerequisite. For example, the brakes need to be pressed to "turn on the car". My task was to create a physical switch that simulated the brakes being pressed on the rig.

To start, I familiarized myself with the rig’s hardware by talking with the manufacturers and learning about CAN protocol. I then learned to inject CAN signals using DBC files and CANalyzer. Searching through Rivian’s confluence pages, I found the network architecture for the lighting rig’s specific model and practiced injecting CAN signals like the left and right blinkers. I had a lot of trouble finding the signals to simulate the brake lights. This was because I wanted to inject signals from the source controller itself. That is, I wanted to simulate the brake pedal being pressed and not just the light turning on. After looking through many pages of Rivian documentation, I discovered that the brake lights had a checksum and CRC counter that needed to be simulated correctly using specific protocols.

To physically inject the CAN signal, I connected an Arduino nano to an MCP2515 chip and transceiver PCB. I then wrote software in C++ to calculate and send the CRC and CAN signals. Finally, I designed and 3D printed an enclosure for the PCBs.Before leaving, I documented how to make the switch and modify the code to send other CAN signals.

<figure>
    <img src="/BrakeLightSwitch.png" width="50%" />
    <figcaption>3D Printed Case for Sending CAN Signals</figcaption>
</figure>

<h3>Automating Jama Test Cases</h3>

For my second intern project, I was tasked with writing test cases for all of the new interior lighting features in Jama. I soon discovered this to be an extremely tedious task and was curious to see if it could be automated. After looking through Rivian documentation, I learned about the process of creating test cases from functional requirements in Jama. In addition, I learned about APIs and how they can be used to access databases. I then decided to write a Python script to automate the process.

I had very minimal coding experience (I’ve only taken one Python class in high school) so it was a fun challenge learning Python. The main challenge I faced was that I needed to parse the functional requirements in Jama. While most people did follow the EARS pattern as per Rivian protocol, most functional requirements were written colloquially so my script needed to be robust enough to handle random human writing errors. After parsing each functional requirement, my Python script generated multiple test cases for each one and organized them into an Excel spreadsheet that can be easily uploaded to Jama. In the end, my Python script was able to create more than 2000 test cases in approximately 5 minutes.

<h3>Conclusions</h3>

This internship was very surprising because of how different and interdisciplinary my projects were. Most of my prior work experience has revolved around physical mechanical designs, so it was a fun challenge learning about CAN protocols, APIs, using Arduinos, and writing software. I enjoy learning new skills and this internship has allowed me to do so.