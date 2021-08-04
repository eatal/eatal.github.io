---
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

- TOC
{:toc}

***

# Accurate Tracking of Aggressive Quadrotor Trajectories

[![image](/images/hropto.jpg){: style="float: right" height="50%" width="34%"}](/images/hropto.jpg){:target="_blank"} High-speed flight is receiving significant attention in robotics and control research.
It is an important problem towards the deployment of fast robotics in obstacle-rich environments where deviation from the reference trajectory can result in a collision.
We focus on very accurate tracking of fast trajectories, e.g., within a few centimeters while maneuvering at speeds up to 50 km/h.
This is challenging, since complex (unsteady) aerodynamics significantly affect the quadcopter dynamics at high speeds.
In contrast, aerodynamics are often completely neglected in quadcopter flight at low speeds.

We leverage incremental nonlinear dynamic inversion (INDI) control to handle unmodeled dynamics.
This method implicitly estimates and corrects aerodynamic forces and momenta without depending on an aerodynamics model.
It thereby eliminates the need for (often time-consuming and complicated) modeling based on flight data, and results in a vehicle-independent controller.
We use the INDI controller to track the trajectory position and yaw, and their derivatives velocity, acceleration, jerk, snap, yaw rate, and yaw acceleration.
Tracking of snap and yaw acceleration is enabled by direct control over the torque applied to the vehicle. To achieve this, we use optical encoders attached to each motor (shown in picture) to measure the motor speeds.

### Publications and Media
{: .no_toc}

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/K15lNBAKDCs" frameborder="0" allowfullscreen="true"> </iframe>
</figure>


* **Tal, E.**, Karaman, S., Accurate Tracking of Aggressive Quadrotor Trajectories using Incremental Nonlinear Dynamic Inversion and Differential Flatness, IEEE Transactions on Control Systems Technology, In press [Video](https://youtu.be/K15lNBAKDCs){:target="_blank"}, [PDF](https://arxiv.org/pdf/1809.04048.pdf){:target="_blank"}

* **Tal, E.**, Karaman, S., Accurate Tracking of Aggressive Quadrotor Trajectories using Incremental Nonlinear Dynamic Inversion and Differential Flatness, IEEE Conference on Decision and Control (CDC), December 2018 [Video](https://
youtu.be/M1lE9MlFmVA){:target="_blank"}, [PDF](/files/CDC18_1876.pdf){:target="_blank"}

<div style="text-align: right"> 
<a href="#site-nav" class="back-to-top">
  Back to Top &uarr;
</a>
</div>

***

# Photorealistic Simulation for Robotics Research

[![image](/images/flightgoggles.jpg){: style="float: right" width="45%"}](/images/flightgoggles.jpg){:target="_blank"} Simulation is essential for development and evaluation of robotics algorithms. Modern algorithms increasingly depend on visual sensors, like stereo cameras, which can be challenging to simulate.
To enable photorealistic simulation of camera imagery, we developed FlightGoggles.
FlightGoggles achieves photorealism by using environment elements based on photogrammetry.
We took thousands of photographs of real-world objects from different angles, and used them to generate photorealistic 3-D models.
The FlightGoggles _Abandoned Factory_ environment contains over a thousand assets, comprised of 84 unique models.

FlightGoggles can be used as a standalone simulation tool, but can also be combined with actual vehicles in flight. In essence, it is as if we give a pair of virtual reality goggles to the quadcopter. We fly the vehicle under motion capture and use its measured position and orientation to determine the frame of the virtual camera. The camera image is rendered in real time and sent to the on-board computer in flight. While the quadcopter is safely flying in our netted flight room, it receives real-time camera images as if it is navigating an obstacle-rich virtual environment.

FlightGoggles was used by teams from around the world during the simulation challenge of the AlphaPilot Autonomous Drone Racing Competition. Teams developed planning, estimation, and control algorithms to participate in a virtual drone race in FlightGoggles. The most successful teams qualified for the racing circuit in which they implemented their algorithms on actual drones.
 

### Publications and Media
{: .no_toc}

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/qoUlbSAiRko" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

* Guerra, W., **Tal, E.**, Murali, V., Ryou, G., Karaman, S., FlightGoggles: Photorealistic Sensor Simulation for Perception-driven Robotics using Photogrammetry and Virtual Reality, IEEE/RSJ International Conference on Intelligent Robots and
Systems (IROS), November 2019 [Video](https://youtu.be/QCnU_M6DhYU){:target="_blank"}, [PDF](https://arxiv.org/pdf/1905.11377.pdf){:target="_blank"}, [Website](https://flightgoggles.mit.edu/){:target="_blank"}, [GitHub](https://github.com/mit-fast/FlightGoggles){:target="_blank"}

* MIT News Office, Researchers develop virtual-reality testing ground for drones, [MIT News](https://news.mit.edu/2018/virtual-reality-testing-ground-drones-0517){:target="_blank"}

* Sayre-McCord, T., Guerra, W., Antonini, A., Arneberg, J., Brown, A., Cavalheiro, G., Fang, Y., Gorodetsky, A., McCoy, D., Quilter, S., Riether, F., **Tal, E.**, Terzioglu, Y., Carlone, L., Karaman, S., Visual-inertial navigation algorithm development using photorealistic camera simulation in the loop, IEEE International Conference on Robotics and Automation (ICRA), May 2018 [Video](https://youtu.be/_VBww8YQuA8){:target="_blank"}, [PDF](/files/SayreMcCordetal_IROS18.pdf){:target="_blank"}

<div style="text-align: right"> 
<a href="#site-nav" class="back-to-top">
  Back to Top &uarr;
</a>
</div>

***

# Black-Box Optimization for Time-Optimal Maneuvering

[![image](/images/bayesopt.png){: style="float: right" height="50%" width="45%"}](/images/bayesopt.png){:target="_blank"} Planning time-optimal quadcopter maneuvers is a challenging and potentially risky task, since these maneuvers approach the physical limitations of the vehicle.
Hence, precise knowledge of the dynamic feasibility constraints is required.
These feasibility constraints can become highly complex in light of high-acceleration flight and aggressive attitude changes.
The demanding maneuvers affect flight dynamics, but also hardware and software for control and state estimation.
Unsteady aerodynamic effects, control and actuation bandwidth, estimation delays etc. need to be considered.
The resulting constrains are not easily expressed in a convenient way and can only be identified through costly flight experiments.

We propose an algorithm for modeling of quadrotor feasibility constraints and generation of time-optimal trajectories based on Gaussian process classification.
The algorithm combines data from analytical approximation, numerical simulation, and real-world flight experiments to efficiently (i.e., using a limited number of flight experiments) find the time-optimal trajectory.

### Publications and Media
{: .no_toc}

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/igwULi_H1Kg" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

* Ryou, G., **Tal, E.**, Karaman, S., Multi-Fidelity Black-Box Optimization for Time-Optimal Quadrotor Maneuvers, The International Journal of Robotics Research (IJRR), July 2021

* Ryou, G., **Tal, E.**, Karaman, S., Multi-Fidelity Black-Box Optimization for Time-Optimal Quadrotor Maneuvers, Robotics: Science and Systems (RSS), July 2020 [Video](https://youtu.be/igwULi_H1Kg){:target="_blank"}, [PDF](https://arxiv.org/pdf/2006.02513.pdf){:target="_blank"}

<div style="text-align: right"> 
<a href="#site-nav" class="back-to-top">
  Back to Top &uarr;
</a>
</div>

***

# Tensor Train Differential Games Dynamic Programming
[![image](/images/pursuit.png){: style="float: right" height="50%" width="45%" margin="10"}](/images/pursuit.png){:target="_blank"} Differential games provide a widely applicable formulation for representing two-sided optimal control problems, e.g., pursuit-evasion or worst-case robust control scenarios.
However, besides some special cases, such as linear-quadratic games, differential games can be challenging to solve exactly.
For this reason, computational methods are often resorted to.
The downside of these algorithms is that they are typically unsuitable to address high-dimensional problems, i.e., problems with a large number of state variables. This is due to the _curse of dimensionality_, which entails an exponential scaling of computational cost and memory requirements with problem dimension.

We leverage the tensor train decomposition to avoid exponential cost. This decomposition can be seen as a multi-dimensional generalization of the singular value decomposition (SVD).
Using the tensor train decomposition, we obtain a rank-limited approximation of the differential game value function at polynomial cost (instead of exponential cost).
This favorable scaling with problem dimension makes our algorithm suitable for addressing high-dimensional problems that would otherwise be infeasible. 

### Publications and Media
{: .no_toc}
* **Tal, E.**, Gorodetsky, A., Karaman, S., Continuous tensor train-based dynamic programming for high-dimensional zero-sum differential games, American Control Conference (ACC), June 2018 [PDF](/files/TalGorodetskyKaraman_ACC2018.pdf){:target="_blank"}

<div style="text-align: right"> 
<a href="#site-nav" class="back-to-top">
  Back to Top &uarr;
</a>
</div>