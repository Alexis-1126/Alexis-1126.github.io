---
title: "2.72 Elements of Mechanical Design"
description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
dateRange: "August 2021 - June 2022"
pubDate: "Sep 12 2022"
heroImage: "/Lathe.png"
badge: "MIT Class"
tags: ["Precision Manufacturing","HTM Model","Measurement & Analysis"]
---

2.72 - Elements of Mechanical Design is a class at MIT taught by Professor Martin Culpepper that focuses on modeling, design, integration, and best practices for use of machine elements such as bearings, bolts, belts, flexures, and gears. The class culminates in a final project where teams of students build a desktop lathe.

<h3>Functional Requirements</h3>

Our team began by defining functional requirements for our lathe. Our main constraints were that the lathe must be repeatable to 50 microns and we had a budget of $200. We were also provided a motor that had a maximum power of 337 W. Given these parameters, we defined functional requirements for the efficiency, stiffness, temperature sensitivity, and dimensions of the lathe. We further broke down these functional requirements into requirements for each system on the lathe (ex. spindle, carriage, etc.). These system requirements acted as checkpoints to ensure we were on track to meet our overall functional requirements.

<h3>Spindle and Cross Slide Design</h3>

We chose an indirect bearing mount architecture for supporting the spindle. We had a slip fit between the spindle and bearing in the back and press fit with the bearing in the front. This allowed for axial thermal expension of the spindle while still constraining the shaft. We applied preload to the bearings with a nut and belleville washer.

To determine the preload value, I compared it's effect on system stiffness, bearing life, and efficiency. Increasing the preload increased the stiffness and decreased the bearing life and efficiency of the lathe. Thus, the minimum preload was limited by our stiffness requirement and the maximum preload was limited by the bearing life and efficiency requirements.

Once we assembled the spindle, we took measurements to verify that it met our functional requirements which it did.

Our cross slide featured a dovetail base actuated by a lead screw. I helped calculate the preload of the gib between the sliding dovetails, leadscrew, and thrust bearing supporting the leadscrew. Similar to the spindle design, I compared the preload's effect on stiffness, efficiency, and lifetime to get a range of values that will satisfy our requirements.

<h3>Homogenous Transfer Matrix (HTM) Model</h3>

To get a sense of how much error we expect our lathe to have, I helped create an HTM Model of the stiffness and deflection of the entire lathe. By approximating the stiffness of each component in the lathe (and using stiffness values we measured), I was able to calculate the total deflection of a part in the spindle under cutting forces. This helped inform us if a specific part was not stiff enough, and we did indeed find out that our tool holder contributed a signficant amount of error to our lathe. We then made modifications to the tool holder's design to increase its stiffness and thus, decrease our lathe's total error.

<h3>Competition and Wrap Up</h3>

When we finished our lathe, we used a Coordinate Measuring Machine (CMM) to measure it and check if it met our functional requirements. We found that the lathe did meet all functional requirements as seen below.
<table>
    <tr>
        <th>Functional Requirement</th>
        <th>Measured Value</th>
    </tr>
    <tr>
        <td>MRR - 0.5 in<sup>3</sup>/min (0.02-0.6in<sup>3</sup>/min)</td>
        <td>0.24 in<sup>3</sup>/min</td>
    </tr>
    <tr>
        <td>Max Cutting Force - 70 N (0 - 140 N)</td>
        <td>Max 118 N</td>
    </tr>
    <tr>
        <td>Spindle Speed - 1300 rpm (1000 - 1300 rpm)</td>
        <td>1050 rpm</td>
    </tr>
    <tr>
        <td>Workable Part Diameter - 0.125" < 1" < 2"</td>
        <td>Max 2" OD</td>
    </tr>
    <tr>
        <td>Workable Part Length - 0.1" - 3.5"</td>
        <td>Max 3.5" length</td>
    </tr>
    <tr>
        <td>Repeatability - Max 50 microns</td>
        <td> < 25 microns in Z and < 25 microns in X </td>
    </tr>
    <tr>
        <td>Accuracy (no functional requirement)</td>
        <td>25 microns</td>
    </tr>
    <tr>
        <td>Input Actuation - 0.25 Nm - 1 Nm</td>
        <td> 0.24 &plusmn 0.03 Nm </td>
    </tr>
    <tr>
        <td>Max Temperature Fluctuation - Max 0.02 C/s </td>
        <td>0.015 &plusmn 2 C/s</td>
    </tr>
    <tr>
        <td>Overall Efficiency - 53% - 65%</td>
        <td>At least 62%</td>
    </tr>
    <tr>
        <td>Size - Max 2'x 4' x 1.5'</td>
        <td> < 19" x 8" x 12" </td>
    </tr>
    <tr>
        <td>Weight - 30 lbs - 60 lbs</td>
        <td>36.3 &plusmn 0.1 lbs</td>
    </tr>
    <tr>
        <td>Stiffness - X,Y > 6&times10<sup>5</sup> N/m and Z > 4&times10<sup>5</sup> N/m </td>
        <td>X - 4.84&times10<sup>5</sup> &plusmn 1.37&times10<sup>5</sup> N/m <br> Y - 3.77&times10<sup>6</sup> &plusmn 1.69&times10<sup>6</sup> N/m <br> Z - 2.65&times10<sup>6</sup> &plusmn 1.70&times10<sup>6</sup> N/m </td>
    </tr>
    <tr>
        <td>External Force - Min 250 N </td>
        <td> > 250 N </td>
    </tr>
</table>

We then participated in a class competition to test the MRR and accuracy of our lathes turning aluminum. We came in 3<sup>rd</sup> place in the MRR race with an MRR of 0.00975 in<sup>3</sup>/s and 2<sup>nd</sup> place in the accuracy race with en error of 0.00124" out of six teams. 

Finally, our lathe experienced a drop test and sledgehammer test to test it's durability and ability to remain repeatable within 50 microns. It was dropped approximately 1 m from the ground and the spindle was hit axially with a sledgehammer. Our lathe passed both these tests.

<h3>Learnings</h3>

This class was a great learning experience to make precision machines. I learned the importance of establishing and validating functional requirements with calculations and measurements. I also learned various analytical skills like calculating design tradeoffs between lifetime, efficiency, compliance, and strength, and creating HTM models to adjust design parameters. In addition, I practiced important engineering skills like machining, formulating process plans, and communicating.