---
title: "Hydrogen Research"
description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
dateRange: "May 2024 - June 2024"
pubDate: "Sep 12 2022"
heroImage: "/HydrogenResearch.png"
badge: "Academic Research"
tags: ["LABView","Instron Testing", "SolidWorks","Lasercutting"]
---

At MIT, I conducted research in the Gear Lab under Professor Amos Winter. The goal of the research is to design pressure vessels to store compressed hydrogen gas. The scope of my project was to prototype the feasibility of aluminum end caps for a hydrogen pressure vessel and create a hydraulic testing rig for more accurate pressure tests.

<h3>Aluminum End Caps</h3>

Previous research focused on the strength between carbon fiber end caps and carbon fiber tubes. For my project, we wanted to explore the use of aluminum end caps since they are easier to manufacture and cheaper than carbon fiber. I manufactured the end caps using a CNC mill, sandblasted the surface, and epoxied it to the carbon fiber tubes. We then performed a tensile test on the joint using an Instron machine.

<figure>
    <img src="/InstronTest.png" width="40%" />
    <figcaption>Instron Test</figcaption>
</figure>

We found that the strength of the aluminum-to-carbon fiber joint was of the same magnitude as the strength of the carbon fiber-to-carbon fiber joint. Because of this, we decided to continue using aluminum end caps for testing the pressure vessels.

<h3>Hydraulic Testing Rig</h3>

My next project was to assemble a hydraulic testing rig. While most of the parts were already ordered and the flow loop designed, there was a lot of preparation to be done on the electrical side. The flow loop contained five pressure sensors and three control valves which I wired-up to an NI cDAQ. We then connected a switch to each valve so that we could easily open them and relieve pressure in the lines. Afterwards, I made a test program in LabView that displayed the pressure values from each pressure sensor (it automatically converted the current signal from the sensor to pressure) and had button controls for opening and closing each valve.

<figure>
    <img src="/LabViewSetUp.png" width="80%" />
    <figcaption>LabView Test UI</figcaption>
</figure>