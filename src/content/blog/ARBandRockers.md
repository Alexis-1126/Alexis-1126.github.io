---
title: "Anti-Roll Bar and Rockers Subsystem Lead"
description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
dateRange: "August 2021 - June 2022"
pubDate: "August 5, 2021"
heroImage: "/Tilt Test.png"
badge: "Project Team"
tags: ["NX", "NX Motion Analysis", "NX Nastran FEA","DFM DFA","CNC Machining", "Waterjet"]
---


The anti-roll bars (ARBs) and rockers are both integral suspension components in a racecar and help to control suspension paramters like roll and ride rate. The rockers lift the car and dampen vibrations while the ARBs makes it easier to drive and prevents the car from rolling over. As the subsystem lead, I was responsible for the entire process of researching, designing, manufacturing, and assembling MY22's (Model Year 2022) rockers and ARBs. By the end of the year, I successfully assembled the rockers on the racecar and manufactured most of the components of the ARBs system. 

<h3>Design and Manufacturing</h3>

To start the design process, I worked with the team's suspension lead to finalize car parameters like roll rate, ride rate, and stiffness. These parameters informed my design requirements including the motion ratio, spring stiffness, and external forces. The rockers had a clamshell design where the car's pushrod and springs were connected by clamping plates. The ARBs featured an adjustable linking arm that connected the rockers to the torsional bar.

I used a top-down modeling approach in NX for designing the subsystems. I communicated frequently with the team's suspension lead and frame lead to ensure my system met packaging constraints. I also used NX Motion Analysis to check the motion ratios and avoid interferences.

<figure>
    <video src="/RockerMR.mp4" width="80%" autoplay mute loop></video>
    <figcaption>Rocker Motion Analysis in NX</figcaption>
</figure>

Once the designs were finalized, I created manufacturing plans. For the rockers, I used both the waterjet and 3 axis CNC machine. I waterjet the outside triangular shape and milled the interior features, holding the triangular stock in a custom, aluminum soft-jaw. For the ARBs, I waterjet the adjustable linking plate. I, unfortunately, didn't have time to machine the torsional bar, since I was placed on another project at the end of the year.

<figure>
    <img src="/FrontRockers.png" width="50%" />
    <figcaption>Front Rockers (clamshell design)</figcaption>
</figure>

Because the rockers' and ARBs' motion ratio were sensitive to their mounting positions, I designed and manufactured a custom jig for welding their tabs onto the frame. The jig ensured that the ARBs mounting and rocker mounting were accurate with respect to each other and that the distance between the springs and rockers were accurate. These were the two factors that heavily impacted the motion ratio of the system. A challenge I faced during this process was manufacturing the jig. The rocker tabs were not on plates parallel to any of the car's axis - they were a couple of degrees offset from the Z-X and X-Y plane. Because of this, the jig could no longer be a machined 2D plate and needed to have a 3D contour. If I could change the design, I would've either constrained the rockers on a plane with no angles or angeled them to a round degree to either use a tapered endmill or angle vice.

<h3>Rockers FEA</h3>

In my initial hand calculations for the rockers, I assumed the frame was entirely rigid and not affected by forces in my system. However, I realized that this was not the case as 1) the frame is not rigid and 2) the rocker's mounting points were not triangulated at nodes of frame tubes. While the 2nd point could've been avoided in CAD, we had already froze the design and machined all the components. Thus, I needed to find a way to alleviate the bending stresses in the frame tubes.

I conducted FEA in NX Nastran. To simplify my model, I converted the tubes and tabs to a 2D mesh and stitched the meshes together to model the welds. I then modeled the fasteners as rigid connections and the rockers and springs as rigid bodies to analyze how the frame tubes will react under peak bump loads. In my initial model, I only included the two frame tubes with tabs and fixed their ends (where they connected to nodes). The bending stresses in this model was too high and so I began refining my model to include the nodes of frame tubes, the supension tabs, and suspension forces. After this, I found that I can add gussets to the tabs and frame tubes to add thickness and prevent it from bending and breaking.

<h3>Learnings</h3>

The rockers system was sucessfully assembled on MY22 in time for the 2022 FSAE Competition. Since the ARBs system wasn't required for the competition (compared to other systems), I was transferred to a different project on the racecar that was more urgent. Overall, it was a great learning experience going through the entire process of designing to manufacturing and assembly. I found that communication was key to a successful system integration on MY22, especially since the rockers affect the suspension, chassis, and even body panel mounting. Looking back, there are many things I would change in my initial design to optimize the manufacturing and assembly process. I would've changed my initial design to have mounting points parallel to a plane (decreasing tab jigging complexity), made the shape of the rockers a common angle to use v clamps instead of custom machined soft jaws, minimized the contact area between the tab and rocker to decrease the friction between them, and placed the mounting tabs at nodes or tell the frame lead to increase the frame thickness. This project has showed me the importance of communication, helped me learn how to design for manufacturing and assembly, and use programs like NX Nastran and NX Motion Analysis.