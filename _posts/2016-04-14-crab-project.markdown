---
layout: post
modalID: modalCrab
permalink: /:categories/:slug/
main_title:  Honours Project - Augmenting a Robotic Model of Fiddler Crab Interaction

thumb_image_url: assets/post_assets/crab/images/original/logo.jpg
images:
  - {
    url: "assets/post_assets/crab/videos/mp4/color_res_1.mp4",
    id: "crab_robot"
  }
  - {
    url: "assets/post_assets/crab/videos/mp4/color_res_2.mp4",
    id: "masked_ommatidia_view"
  }
  - {
    url: "assets/post_assets/crab/images/original/123.jpg",
    id: "overhead_view"
  }
  - {
    url: "assets/post_assets/crab/videos/mp4/birdeye_result.mp4",
    id: "fast_features"
  }
  - {
    url: "assets/post_assets/crab/videos/mp4/SLAM_res_1.mp4",
    id: "filtered_view"
  }
  - {
    url: "assets/post_assets/crab/videos/mp4/SLAM_res_2.mp4",
    id: "color_picker_example"
  }
category: projects
course_name: Honours Project
project_title: Augmenting a Robotic Model of Fiddler Crab Interaction
thumb_text: Improvements to Localization system of a robotic crab using Optical Flow
collaborators:
tech:
  - C++
  - SLAM
  - OpenCV
  - Python
  - Numpy
  - Linux
size: extra-large

---

<div class="post-content-markdown">

The robotic model of a fiddler crab is a four-wheeled vehicle, capable of omnidirectional movement, foraging behavior, predator detection, evasion, and retreat to the burrow. It uses a two-sided fisheye camera (RICOH THETA S) and a specific crab-eye filter, specifically chosen and designed to mimic the visual system of the crab.
{: .text-left}

As my final project in University of Edinburgh, I looked for ways to improve the system by introducing new features, related to modeling the real crabs and improving the reliability of the current system. The list of contributions I made is as follows:
{: .text-left}

* Improved the foraging behavior of the robot. For as much as the path integration allows it, the robot attempts to orient itself towards its burrow. Furthermore, the foraging behavior no longer relies on random walk and more closely matches the behavior of crabs in nature.
* Developed several tools for the system:
  *  Color picking tool allows to pick and store color information of color ranges. The values are integrated into the object detection framework, allowing quick predator and burrow color tweaking. Code Repository: [GitLab](https://gitlab.com/LinasKo/camera_color_picker){:target="_blank"}
  * Self-masking tool masks the crab from itself, preventing it from mistaking colors of its chassis and wires for the burrow. This replaced the previous ad-hoc solution, where the crab was covered with post-it notes and paper.
  * Designed and implemented an overhead tracker of the robot, based on visual markers, on the robot. It was used to gather and correlate observed robot rotation with optical flow data from the robot. If needed, additional data such as robot’s rotation, estimated by the path integration system, can be tracked and analyzed.
* Experiments were performed with an elevated stationary object, used as a reference, aimed to help the robot estimate its rotation. Results have shown that with the crab eye filter, the robot is incapable of detecting even a bright A4 sheet, 2.20 meters away from it.
* I have found and corrected two bugs in the previously developed robot’s system, that impacted the way movement trajectory was calculated.
* Implemented, but did not achieve success of rotation and translation recovery, based on optical flow and Essential Matrix decomposition. I believe this is due to the errors introduced when dewarping a fisheye image.
* Measured the correlation between observed optical flow and pure rotations of the robot. The relation is (surprisingly) linear. However, the function is location specific, meaning that without translation tracking or additional optimization, the usage of first-principles-based optical flow does not improve the path integration system.
{: .text-left}

Ultimately, the project explored different way that the path integration system could be improved, focusing on optical flow. Auxiliary tools that were developed in the process open up new ways of interacting with the robot, as well as covering some weaker points of the previous system.
{: .text-left}

<br>
Code Repository: [GitHub](https://github.com/gmission-official/YOLOv8-Semantic-Segmentation){:target="_blank"}
{: .text-center}

</div>
