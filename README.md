<div align="center">

<!-- Header Banner -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,12,22&height=180&section=header&text=Abhishek%20Dubasi&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=32&desc=Mechatronics%20Enthusiast&descSize=18&descAlignY=52"/>

<!-- Animated Typing -->
<a href="https://github.com/AbhishekDubasi09"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=false&repeat=true&width=820&height=35&lines=ChromaPick+%7C+Franka+Colour+Sorter+in+ROS+2;PX4+Offboard+Timing+Study;Driver+Monitoring+Validation;Sensor+Data+Quality+Checks;VR+Driving+Simulator+in+Unity+6" alt="Typing SVG" /></a>

<!-- Social Badges -->
<p>
<a href="https://www.linkedin.com/in/abhishek-d-1051661b7/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="mailto:dubasiabhishek@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
<img src="https://komarev.com/ghpvc/?username=AbhishekDubasi09&label=Profile%20Views&color=0e75b6&style=for-the-badge" alt="Profile views"/>
</p>

</div>

---

## About Me

- **M.Eng. student** in Mechatronic and Cyber-Physical Systems at **TH Deggendorf**
- **Thesis (current, simulation only):** phase-aware curation of teleoperation demonstrations for precision manipulation, with **MuJoCo** and **robosuite**
- Working with **ROS 2**, **Gazebo**, **MoveIt 2**, **PX4 SITL** and **Unity**
- Every project below links to its code, its results and its limits

---

## <img src="https://img.shields.io/badge/-F7DF1E?style=flat-square" height="18"/> Project Work

<table>
  <tr>
    <td align="center" width="25%">
      <a href="https://github.com/AbhishekDubasi09/Franka_Panda_Color_Sorting_Robot">
        <img src="https://img.shields.io/badge/ChromaPick-Colour%20Sorting-blue?style=for-the-badge" alt="ChromaPick"/>
        <br/><sub><b>Camera Geometry Vision</b></sub>
      </a>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/AbhishekDubasi09/px4-offboard-timing-study">
        <img src="https://img.shields.io/badge/PX4-Offboard%20Timing-green?style=for-the-badge" alt="PX4"/>
        <br/><sub><b>Setpoint Rate Study</b></sub>
      </a>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/AbhishekDubasi09/driver-monitoring-validation">
        <img src="https://img.shields.io/badge/Driver%20Monitoring-Validation-orange?style=for-the-badge" alt="Driver monitoring"/>
        <br/><sub><b>Scored Against Ground Truth</b></sub>
      </a>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/AbhishekDubasi09/sensor-data-quality-checks">
        <img src="https://img.shields.io/badge/Sensor%20Data-Quality%20Checks-purple?style=for-the-badge" alt="Sensor checks"/>
        <br/><sub><b>Five Plausibility Checks</b></sub>
      </a>
    </td>
  </tr>
</table>

### ChromaPick: Franka Panda Colour Sorter

Enhancement of the open-source Franka sorter by **MechaMind Labs** (credit in the README). Simulation only:

- **Camera geometry** turns each pixel into a ray from the camera pose (TF) and finds where it meets the table, in place of hand-tuned constants
- **Adaptive HSV** corrects white balance and contrast before colour thresholds and takes the centroid of the lit top face
- **Multi-colour sorting** with `target_colors:=RGB`, one drop position per bin
- **Evaluation scripts** compare the detectors with the true object positions from Gazebo and run complete sorting trials
- **New work cell** built from SDF primitives: a table, three pucks and three bins
- **Result over 31 layouts:** mean error **89.6 mm to 1.1 mm** in the original scene, **93 of 93** objects found against **31 of 93** in the new scene, **11 of 12** pucks in the right bin over four runs

### PX4 Offboard Timing Study

What does the quality of the setpoint stream do to offboard flight? ROS 2 Jazzy, PX4 SITL and a Gazebo x500:

- **Study node:** arm, offboard, takeoff, hold, 90 degree turn, velocity square, land, with configurable stream degradation and a 100 Hz CSV log
- **Teleoperation node** for joystick or keyboard with deadzone and limits
- **Rate versus error:** the tracking error rises as the stream rate falls. **1 Hz lost offboard, 1.5 Hz and above did not**
- **One gap in a 50 Hz stream:** gaps up to **0.9 s** were tolerated, **1.1 s and longer** always lost offboard (default timeout 1.0 s, three runs per bar)
- **Flight videos**, findings and caveats are in the repository

### Driver Monitoring Validation

A simulated driver is filmed by virtual cameras in Unity. A Python pipeline with **MediaPipe** and **OpenCV** tracks gaze, glances, hands and reaction time, and the simulator's own ground truth scores it:

- **Gaze angle:** mean absolute error **1.17 degrees**, zone correct in **99.9 %** of 718 steady frames
- **Blinks:** 17 detected, 17 rendered
- **Pipeline speed:** 204 ms median from capture to analysed frame, at 19.4 frames per second
- **Delay analysis:** the reaction time came out late by 114 ms and 196 ms, and shifting the true gaze by 55 ms cuts the error from 2.82 to 1.36 degrees RMSE
- **Scope:** simulated and scripted, one subject, one session

### Sensor Data Quality Checks

Python, pandas and NumPy:

- **Five checks:** time alignment, range, rolling z-score, frozen value and cross-check
- **Flags, never deletes:** each flagged sample stays in the data with its reason
- **Synthetic run:** 3000 samples at 10 Hz, 61 flagged (2.03 %), including an injected spike and a stuck stretch

**Skills used across the projects:**
`ROS 2` · `Gazebo` · `MoveIt 2` · `PX4 SITL` · `TF2` · `OpenCV` · `MediaPipe` · `Unity` · `Python` · `C#` · `pandas` · `NumPy` · `Ground-Truth Evaluation` · `Timing Analysis`

---

## <img src="https://img.shields.io/badge/-58A6FF?style=flat-square" height="18"/> Featured Projects

### <img src="https://img.shields.io/badge/-blueviolet?style=flat-square" height="14"/> Robotics & Simulation

<table>
  <tr>
    <td width="50%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/Franka_Panda_Color_Sorting_Robot"> ChromaPick</a></h3>
      <p align="center">Franka Panda colour sorter with camera geometry vision</p>
      <p align="center">
        <img src="https://img.shields.io/badge/ROS%202-22314E?style=flat-square&logo=ros&logoColor=white"/>
        <img src="https://img.shields.io/badge/MoveIt%202-2D3E50?style=flat-square"/>
        <img src="https://img.shields.io/badge/Gazebo-FF6F00?style=flat-square"/>
      </p>
    </td>
    <td width="50%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/px4-offboard-timing-study"> PX4 Offboard Timing Study</a></h3>
      <p align="center">Setpoint stream rate and gaps against tracking and failsafe</p>
      <p align="center">
        <img src="https://img.shields.io/badge/ROS%202-22314E?style=flat-square&logo=ros&logoColor=white"/>
        <img src="https://img.shields.io/badge/PX4-0B2A4A?style=flat-square"/>
        <img src="https://img.shields.io/badge/Gazebo-FF6F00?style=flat-square"/>
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" colspan="2">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/Railway-Track-Monitoring-Robot"> Railway Track Monitoring Robot</a></h3>
      <p align="center">Bachelor thesis prototype: remote-controlled Arduino robot with live video and a cleaning brush</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white"/>
        <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
        <img src="https://img.shields.io/badge/Bluetooth-HC--05-0082FC?style=flat-square"/>
      </p>
    </td>
  </tr>
</table>

### <img src="https://img.shields.io/badge/-00D4AA?style=flat-square" height="14"/> Vehicle Safety & Validation

<table>
  <tr>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/driver-monitoring-validation"> Driver Monitoring Validation</a></h3>
      <p align="center">Camera-based driver monitoring scored against simulator ground truth</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white"/>
        <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square"/>
        <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>
      </p>
    </td>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/VehicleSafetySim_2026"> VehicleSafetySim 2026</a></h3>
      <p align="center">VR driving simulator for Euro NCAP style AEB pedestrian scenarios</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Unity%206-000000?style=flat-square&logo=unity&logoColor=white"/>
        <img src="https://img.shields.io/badge/OpenXR-FF6600?style=flat-square"/>
      </p>
    </td>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/Virtual-Reality_Driver_Perspective_Safety_Simulator"> Driver Perspective Safety Simulator</a></h3>
      <p align="center">Coursework VR simulation for AEB testing on Meta Quest 3</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white"/>
        <img src="https://img.shields.io/badge/Meta%20Quest%203-0467DF?style=flat-square"/>
      </p>
    </td>
  </tr>
</table>

### <img src="https://img.shields.io/badge/-F7DF1E?style=flat-square" height="14"/> Data & Computer Vision

<table>
  <tr>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/sensor-data-quality-checks"> Sensor Data Quality Checks</a></h3>
      <p align="center">Plausibility checks for sensor time series</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
        <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>
      </p>
    </td>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/pupil-detection-mediapipe-openCV"> Eye Detection</a></h3>
      <p align="center">Real-time eye detection and cropping from a webcam</p>
      <p align="center">
        <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square"/>
        <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>
      </p>
    </td>
    <td width="33%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/hand-tracking-mediapipe"> Hand Tracking</a></h3>
      <p align="center">Real-time hand tracking with 21 landmarks per hand</p>
      <p align="center">
        <img src="https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square"/>
        <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>
      </p>
    </td>
  </tr>
</table>

<details>
<summary><b>ChromaPick: Full Results</b></summary>
<br/>

Detection error is the distance between where a detector puts an object and where Gazebo says it is. Simulation, 31 layouts each time.

| Scene | Measure | Original detector | New detector |
|:--|:--|:--|:--|
| Original scene (boxes) | Mean error | 89.6 mm | 1.1 mm |
| Original scene (boxes) | Worst case | 175.8 mm | 1.7 mm |
| New scene (pucks) | Objects found | 31 of 93 | 93 of 93 |
| New scene (pucks) | Mean error | 82.6 mm (red only) | 1.1 mm |
| New scene (pucks) | Worst case | 163.4 mm | 1.4 mm |

Complete sorting runs in the new scene: four random layouts, **11 of 12 pucks** ended up in the bin for their colour. Twelve pucks are too few for a tight success rate, and all of it is simulation.

</details>

### <img src="https://img.shields.io/badge/-76B900?style=flat-square" height="14"/> CAD & Design

<table>
  <tr>
    <td width="50%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/CATIA-Designs"> CATIA Designs</a></h3>
      <p align="center">CATIA V5 part and assembly models</p>
    </td>
    <td width="50%">
      <h3 align="center"><a href="https://github.com/AbhishekDubasi09/Siemens_NX_part_samples"> Siemens NX Samples</a></h3>
      <p align="center">Siemens NX Student Edition parts, drawings and assemblies</p>
    </td>
  </tr>
</table>

---

## Results & Documentation

| Title | Type | Link |
|:------|:-----|:----:|
| **PX4 Offboard Timing Study**: findings and caveats | Study | [🔗](https://github.com/AbhishekDubasi09/px4-offboard-timing-study) |
| **ChromaPick**: results and limitations | Evaluation | [🔗](https://github.com/AbhishekDubasi09/Franka_Panda_Color_Sorting_Robot) |
| **Driver Monitoring Validation**: session report and delay analysis | Validation | [🔗](https://github.com/AbhishekDubasi09/driver-monitoring-validation) |
| **Railway Track Monitoring Robot**: Bachelor thesis report | Thesis | [🔗](https://github.com/AbhishekDubasi09/Railway-Track-Monitoring-Robot) |

---

## Tech Stack

<div align="center">
<table>
  <tr>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=py" width="48" height="48" alt="Python" /><br>Python</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=cpp" width="48" height="48" alt="C++" /><br>C++</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=cs" width="48" height="48" alt="C#" /><br>C#</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=unity" width="48" height="48" alt="Unity" /><br>Unity</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=opencv" width="48" height="48" alt="OpenCV" /><br>OpenCV</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=ros" width="48" height="48" alt="ROS 2" /><br>ROS2</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=arduino" width="48" height="48" alt="Arduino" /><br>Arduino</td>
  </tr>
  <tr>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=linux" width="48" height="48" alt="Linux" /><br>Linux</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=git" width="48" height="48" alt="Git" /><br>Git</td>
    <td align="center" width="96"><img src="https://skillicons.dev/icons?i=github" width="48" height="48" alt="GitHub" /><br>GitHub</td>
    <td align="center" width="96"><img src="https://img.shields.io/badge/MuJoCo-4285F4?style=flat-square&logoColor=white" height="48" alt="MuJoCo" /><br>MuJoCo</td>
    <td align="center" width="96"><img src="https://img.shields.io/badge/Gazebo-FF6F00?style=flat-square" height="48" alt="Gazebo" /><br>Gazebo</td>
    <td align="center" width="96"><img src="https://img.shields.io/badge/MoveIt%202-2D3E50?style=flat-square" height="48" alt="MoveIt 2" /><br>MoveIt 2</td>
    <td align="center" width="96"><img src="https://img.shields.io/badge/PX4-0B2A4A?style=flat-square" height="48" alt="PX4" /><br>PX4</td>
  </tr>
</table>
</div>

---

## GitHub Stats

<div align="center">
  <img src="https://streak-stats.demolab.com/?user=AbhishekDubasi09&theme=tokyonight&hide_border=true" alt="GitHub streak stats"/>
</div>

---

<div align="center">

## Let's Connect

<p>
<a href="https://www.linkedin.com/in/abhishek-d-1051661b7/"><img src="https://img.shields.io/badge/LINKEDIN-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="mailto:dubasiabhishek@gmail.com"><img src="https://img.shields.io/badge/EMAIL-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
<a href="https://github.com/AbhishekDubasi09?tab=repositories"><img src="https://img.shields.io/badge/GITHUB-REPOS-181717?style=for-the-badge&logo=github&logoColor=white" alt="Repositories"/></a>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,12,22&height=100&section=footer"/>

</div>
