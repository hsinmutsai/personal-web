---
title: CELLI - Indoor Positioning Using Polarized Sweeping Light Beams [MobiSys'17]

notitle: false

description: |
  CELLI uses a single luminary to project a large number of fine-grained, polarized, yet imperceptible light beams to the ground for indoor positioning. The system can achieve a 2.7cm median 2D error.


layout: project
image: img/project/celli.png
last-updated: 2017-06-23
image-link: img/project/celli.png
---



Existing visible light positioning (VLP) systems leverage the high image resolution of a receiving camera to support high position- ing accuracy. However, power-hungry cameras might not always be applicable for many scenarios, such as smart factories, in which small objects require to be accurately localized and tracked. In this paper, we introduce CELLI, an indoor VLP system that only uses a single luminary as the transmitter and requires only a simple light sensor to achieve an extremely high accuracy with centimeter-level error. The key idea is to provide the spatial resolution capabil- ity from the transmitter instead of the receiver, so that the com- plexity of the receiver can be minimized. In particular, a small LCD is installed at the transmitter to project a large number of nar- row and interference-free polarized light beams to different spatial cells. A receiving light sensor identifies its located cell by detect- ing the unique polarization-modulated signals projected to that cell. CELLI further incorporates a number of novel designs to overcome the technical challenges such as reducing the positioning latency, which is typically limited by the long optical response time of an LCD, and transforming a cell coordinate to the global 3D position using only a single light. We have prototyped our design using off-the-shelf optical and electrical components, and experimentally shown that CELLI achieves a median 3D positioning error less than 11.8 cm and a median 2D positioning error to less than 2.7 cm.


This is a project in collaboration with [Prof. Kate Lin](https://people.cs.nctu.edu.tw/~katelin/) at National Chiao Tung University.

The work is presented in ACM MobiSys 2017 as a full paper and won best demo runner-up at the conference. [[DOI]](https://doi.org/10.1145/3081333.3081352)