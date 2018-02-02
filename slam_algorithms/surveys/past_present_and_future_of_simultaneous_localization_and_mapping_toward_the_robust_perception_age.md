## Past, Present, and Future of Simultaneous Localization and Mapping: Toward the Robust-Perception Age

- [Upper Level](README.md)

Source [PDF](https://arxiv.org/pdf/1606.05830.pdf)

#### Summary

- present the "de-facto" standard formulation of for SLAM
- review robustness and scalability in long-term mapping
- review metric and sematic representations for mapping
- review theoretical performance guarantees
- review active SLAM and exploration
- answer two questions: "Do robots need SLAM", "Is SLAM solved"

The paper focuses on metric and sematic SLAM. For topological and vision SLAM, refer to the survey "Visual place recognition: A survey " [PDF](http://www.cvlibs.net/projects/autonomous_vision_survey/literature/Lowry2016TR.pdf).

#### Terminologies

- priori: the location of a set of landmarks (beacons, GPS)

#### Ages of SLAM History

- classical age
  - 1986 - 2004, 
  - the introduction of the main probabilistic formulations for SLAM
  - approaches based on extended Kalman Filters, Particle Filters and maximum likelihood estimation
- algorithmic-analysis age
  - 2014 - 2015
  - studied the observability, convergence, and consistency of SLAM
- robust-perception age
  - 2015 - now
  - characteristics
    - robust performance
      - low failure rate for an extended period of time in a broad set of environments
      - the system includes fail-safe mechanisms and has self-tuning capabilities
    - high-level understanding
      - beyond geometry reconstruction
    - resource awareness
      - tailored to the available sensing and computational resources, and provided means to adjust the computation load
    - task-driven perception
      - able to select relevant perceptual information and filter out irrelevant sensor data in order to support the task the robot has to perform

#### Manifold Aspects that SLAM Involved

- front-end: computer vision, signal-processing
- back-end: geometry, graph theory, optimization, and probabilistic estimation


#### The Importance of Loop Closure SLAM

Loop closure enables SLAM to gain a true topology of the environment.

> A robot performing odometry and neglecting loop closures interprets the world as an "infinite corridor" in which the robot keeps exploring new areas indefinitely. A loop closure event informs the robot that this "corridor" keeps intersecting itself.

#### Author's View towards SLAM' Maturity

Maturity should be considered with the respect to robot/environment/performance combination.

- robot
  - type of motion, e.g., dynamics, maximum speed
- environment
  - planner or 3-D
  - presence of natural or artificial landmarks
  - amount of dynamic elements
  - amount of symmetry
  - risk of perceptual aliasing
- performance requirement
  - accuracy of the estimation of robot state
  - accuracy, and type of representation of the environment, e.g., landmark-based or dense
  - success rate
  - estimation latency
  - maximum size of the mapped area

#### Introductory Papers

- Simultaneous Localisation and Mapping (SLAM): Part I The Essential Algorithms [PDF](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.477.7077&rep=rep1&type=pdf)
- Simultaneous Localisation and Mapping (SLAM): Part II State of the Art [PDF](https://pdfs.semanticscholar.org/27d4/6db7ed4e96944080052b761c62102f26b23f.pdf)

#### Maximum a Posteriori (MAP) Estimation

Refer to "Section II: ANATOMY OF A MODERN SLAM SYSTEM" of the paper.

