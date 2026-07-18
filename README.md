<!-- DRAFT — working copy for the github.com/shyam-sreenivasan profile README. Not yet staged to GitHub. -->

### About Me

👋 Hey, I'm Shyam — a software engineer and team lead. I've spent 6+ years building distributed systems, data infrastructure, and ML platforms in production. Now I'm bringing that same systems depth to physical AI.

---

### 🧠 Areas of Interest

- Data infrastructure, ML platforms, and observability at production scale.
- Core robotics problems — perception, SLAM, motion planning.

If this is your world too, I'd like to talk.

---

### 🚧 Currently Working On

**Language Grounding in VLA Models: Signal or Shortcut?**

A Vision-Language-Action model could be reading the scene and ignoring its instruction entirely, and you'd never know. I built a causal evaluation harness on LIBERO that holds the scene fixed and perturbs only the instruction, to isolate which one the policy actually uses. Baseline on SmolVLA-450M: 55% task success. Next: run the perturbation conditions and see where that number moves.

[GitHub →](https://github.com/shyam-sreenivasan/VLA-Causal-Language-Grounding)

---

### 🤖 Selected Robotics and AI Projects

<table>
<tr>
<td width="33%" valign="top">

**Multi-Sensor Fusion Pipeline**

Camera/LiDAR/GPS fusion for AV perception — sub-5px reprojection accuracy.

[GitHub →](https://github.com/shyam-sreenivasan/KITTI-Perception-Pipeline)

<details>
<summary>Read more</summary>
<br>

An autonomous mobile robot's cameras, LiDAR, and GPS disagree slightly about where things are, and a planner can't act on data it can't trust. This is the foundation layer that fixes that: synced, validated, calibrated sensor fusion.

- **Domain:** Self-driving cars · **Dataset:** KITTI
- **Sensors:** Velodyne LiDAR, stereo cameras, GPS/IMU
- **Result:** Sub-5px LiDAR-to-camera reprojection accuracy, 85% point visibility

</details>

</td>
<td width="33%" valign="top">

**Stereo Camera Health Monitor**

Detecting the point where stereo SLAM degrades to no better than mono — 80% accuracy.

[GitHub →](https://github.com/adenm-10/eece5554_final_project/tree/pipeline)

<details>
<summary>Read more</summary>
<br>

A stereo camera silently degrading is worse than one that fails outright — SLAM keeps running with no signal anything's wrong until tracking collapses. Hypothesis: there's a detectable crossover point where stereo degrades to no better than mono, before failure happens. I designed the research question, the severity metric, and the ResNet18+GRU model; a team of 5 ran the experiments on that platform.

- **Domain:** Visual SLAM · **Dataset:** TUM-VI
- **Result:** Distinct failure signatures across 5 degradation types; health monitor detects the crossover point at 80% accuracy

</details>

</td>
<td width="33%" valign="top">

**Dubins-Constrained RRT\* Motion Planning**

Do published RRT* advantages hold under real Ackermann steering constraints?

[GitHub →](https://github.com/shyams612/RRTStarVariantsComparisonOnAckermanLikeConstraint)

<details>
<summary>Read more</summary>
<br>

Better RRT* variants are usually validated assuming holonomic motion — a robot that can move in any direction instantly. Real Ackermann-steered vehicles can't. Question: do the published advantages hold once that constraint is added back in? With a team of 3, I designed the shared abstractions and implemented the reference non-holonomic version; teammates built the rest on top.

- **Domain:** Autonomous ground vehicles (Ackermann steering)
- **Compared:** RRT*, Bi-RRT*, P-RRT* — holonomic vs. Dubins-constrained, on time/success rate/path length/nodes explored
- **Result:** Ranking mostly held — Bi-RRT* stayed fastest and most reliable — but P-RRT*'s potential-field guidance actively conflicted with the curvature constraint, while Bi-RRT*'s search strategy adapted well

</details>

</td>
</tr>
</table>

---

### 📚 Elsewhere

I like breaking hard technical ideas down to first principles and explaining them simply — API retry strategies, write-ahead logs, the OSI model, design patterns, ML fundamentals. Some of that is written up on [Medium](https://medium.com/@shyamsreeni.612), some of it's on [YouTube](https://www.youtube.com/@minuteml9114).

---

<!-- Next up: VLA -->
