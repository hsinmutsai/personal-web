---
title: Lampshade - Augmenting Indoor Inertial Tracking with Light [MobiSys'18]

notitle: false

description: |
  We use polarizer and everyday transparent tape to create a lampshade that helps indoor inertial tracking to achieve centimeter-level accuracy.


layout: project
image: img/project/lampshade.png
last-updated: 2018-06-15
image-link: img/project/lampshade.png
---


Inertial measurement unit (IMU) has long suffered from the problem of integration drift, where sensor noises accumulate quickly and cause fast-growing tracking errors. Existing methods for calibrating IMU tracking either require human in the loop, or need energy- consuming cameras, or suffer from coarse tracking granularity. We propose to augment indoor inertial tracking by reusing existing indoor luminaries to project a static light polarization pattern in the space. This pattern is imperceptible to human eyes and yet through a polarizer, it becomes detectable by a color sensor, and thus can serve as fine-grained optical landmarks that constrain and correct IMU’s integration drift and boost tracking accuracy. Exploiting the birefringence optical property of transparent tapes – a low- cost and easily-accessible material – we realize the polarization pattern by simply adding to existing light cover a thin polarizer film with transparent tape stripes glued atop. When fusing with IMU sensor signals, the light pattern enables robust, accurate and low-power motion tracking. Meanwhile, our approach entails low deployment overhead by reusing existing lighting infrastructure without needing an active modulation unit. We build a prototype of our light cover and the sensing unit using off-the-shelf components. Experiments show 4.3 cm median error for 2D tracking and 10 cm for 3D tracking, as well as its robustness in diverse settings.

This is a project in collaboration with [Prof. Kate Lin](https://people.cs.nctu.edu.tw/~katelin/) at National Chiao Tung University and [Prof. Xia Zhou](https://home.cs.dartmouth.edu/~xia/) at Dartmouth University.

The work is presented in ACM MobiSys 2018 as a full paper. [[DOI]](https://doi.org/10.1145/3210240.3210340)