---
layout: post
modalID: modalUdacityLaneLineDetection2
permalink: /:categories/:slug/
main_title: 고급 차선 감지

thumb_image_url: assets/post_assets/udacity-lane-line-detection-2/videos/gif/final_project_video.gif
images:
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/videos/gif/final_project_video.gif",
    caption: "A fragment of the final submission video",
    id: "final_project_video"
  }
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/videos/gif/challenge_video.gif",
    caption: "A clip of the challenge video",
    id: "challenge_video"
  }
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/images/compressed/line_curvature_example.png",
    caption: "An visual example of the sliding window algorithm, used to find the pixels belonging to each lane line. Here, polynomial functions were also fit to the lines, estimating the curvature.",
    id: "line_curvature_example"
  }
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/videos/gif/best__edge__threshold__sob25_m30-_L_d-09__closed__harder_challenge_video.gif",
    caption: "The final threshold applied to the harder challenge video. Observe that the lane lines can be seen even with all the noise in the system.",
    id: "thresh_harder_challenge_video"
  }
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/videos/gif/best__edge__threshold__sob25_m30-_L_d-09__closed__challenge_video.gif",
    caption: "The final threshold applied to the challenge video. Observe the line in the middle of the road, separating the two types of asphalt used in the road.",
    id: "thresh_challenge_video"
  }
  - {
    url: "assets/post_assets/udacity-lane-line-detection-2/images/compressed/Variance-based__line__selection.png",
    caption: "Variance-based line correction. The green dot on the blue line is placed based not on the width at that point, but on a fixed distance from the green point on the right line",
    id: "variance-based-line-selection"
  }
category: projects
project_title: "고급 차선 감지"
thumb_text: 고급 차선 감지
tech:
  - Computer vision
  - OpenCV
  - Python
  - Numpy

---

<div class="post-content-markdown">

고급 차선 인식 프로젝트는 자율주행차를 위한 컴퓨터 비전 시스템입니다. OpenCV와 Python을 사용하여 개발되었으며, 다양한 도로 환경에서 차선을 정확하게 감지하는 것이 목표였습니다. 이미지 처리 파이프라인은 카메라 왜곡 보정, 채도 채널 추출, 소벨 커널을 이용한 엣지 검출 등 여러 단계로 구성되어 있습니다. 기본적인 도로 환경에서는 잘 작동했지만, 그림자가 있거나 날씨가 흐린 상황, 도로 균열이 있는 경우, 또는 급격한 곡선 구간에서는 차선 인식에 어려움이 있었습니다. 이 프로젝트를 통해 실제 도로 환경에서의 컴퓨터 비전 문제의 복잡성을 잘 보여주었습니다.

<br>
Code Repository: [GitHub](https://github.com/Harry-KIT/CarND-Advanced-Lane-Lines){:target="_blank"}
{: .text-center}

</div>
