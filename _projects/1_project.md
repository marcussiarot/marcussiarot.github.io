---
layout: page
title: Team Robotic Space Exploration (RoSE)
description: Avionics Team
img: assets/img/rover.jpg
importance: 1
category: SCHOOL
related_publications: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rose_logo.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rover_two.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/side_rover.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


<p><strong>Goals:</strong><br>
  The RoSE team designs and builds a Mars-style rover to compete in the University Rover Challenge (URC) which takes place in Hanksville, Utah.
  It is a global competition that tests rover performance in autonomous navigation, scientific analysis, equipment servicing, and terrain traversal. 
  The project emphasizes long-term collaboration, technical skill development, and mentorship among undergraduates across multiple disciplines.
</p>

<p><strong>Core Focus Areas:</strong><br>
  Systems Integration · Robotics · Embedded Systems · Field Testing
</p>

<p><strong>Project Areas:</strong><br>
  We work on mechanical design, power and battery systems, remote communication, autonomous navigation, and software integration to meet the rigorous demands of the URC.
</p>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/team.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/interact.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Team photo of those who flew up to Utah (missing a good amount of people) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Right: Rover completing equipment servicing challenge
</div>

The team was able to qualify and compete in the URC challenge and I had the opportunity to compete and travel with the team.
It was a great experience filled with a lot of unexpected obstacles that had to be overcome in a short period of time and with limited resources.
One of the largest issues that we had was replacing equipment that stopped working and broke.
It was a very far drive in and out of Hanksville and multiple trips had to be taken just to reach a store that sold the equipment needed.
Overall, I learned a lot from this trip including the importance of communication to not only resolve any issues but for improvement of efficiency.  
It was also very interesting to speak to other teams from around the world and learn about how their approaches were similar and/or varied.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/diagram.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Above is a picture of the latest power diagram while I was on the team.  Note the color coordination and various voltages supplied to each component.
All the power comes from the battery which goes first to a power distribution board (PDB).  
A large portion of the power first travels through a fuse box as a safety device that limits current and prevents damage.
The PDB only had 5V, 12V, and live (battery) output voltage terminals so we used two buck converters to safely convert any voltages to certain thresholds.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/battery.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/full_battery.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Battery Diagram &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Right: Picture of the battery in case
</div>

We selected and ordered Molicel 21700 P45B 4500mAh lithium-ion cells for the battery.  
Each cell is 3.6V nominal.  We designed the battery to have 8 cells in series and 4 rows of cells in parallel (8S4P).
To connect the parallel rows, nickel strips were spot welded to the cells and for the series combinations, wires and connectors were used.
For the series connections, wires were used to provide modularity to allow the cells to be seperated for safety and ease if cells need to be replaced.
We also needed to be able to easily seperate the battery cells when flying the rover to and from Utah (from Hawaii).  
The battery utilizes a Flipsky Battery Management System (BMS) that will act as a fail-safe.
If the battery voltage goes below a certain threshold (that could damage the batteries), the BMS will prevent any power from being outputted.
We also have a balance charger that charges each parallel branch of cells simultaneously for safe and efficient charging.
