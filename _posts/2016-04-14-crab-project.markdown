---
layout: post
modalID: modalCrab
permalink: /:categories/:slug/
main_title:  OpenCV 및 ORB-SLAM2 시스템 구현 연구

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
project_title: OpenCV 및 ORB-SLAM2 시스템 구현 연구
thumb_text: Improvements to Localization system of a robotic crab using Optical Flow
collaborators:
tech:
  - C++
  - SLAM
  - OpenCV
  - Python
  - Numpy
  - Linux

---

<div class="post-content-markdown">

OpenCV 구현 프로젝트의 경우, 다음과 같은 네 가지 주요 기능을 C++로 구현했습니다:

1. 컬러 히스토그램 역투영: 이미지에서 특정 영역의 색상 분포를 분석하고, 이를 기반으로 유사한 색상 영역을 검출하는 알고리즘을 구현했습니다. YCrCb 색상 공간을 활용하여 보다 정확한 색상 검출이 가능하도록 했습니다.
2. HSV 기반 색상 분할: HSV 색상 공간에서 색상(Hue)과 채도(Saturation) 값을 트랙바로 조절하여 실시간으로 특정 색상 영역을 분할할 수 있는 시스템을 구현했습니다.
3. 영상 원근 변환: 차량 전방 카메라로 촬영된 영상에서 특정 영역을 Birds-eye view로 변환하는 원근 변환을 구현했습니다. 네 개의 참조점을 이용하여 투시 변환 행렬을 계산하고 적용했습니다.
4. 숫자 인식 시스템: 템플릿 매칭 방식을 사용하여 이미지 내의 숫자를 인식하는 시스템을 구현했습니다. 외곽선 검출과 영역 분할을 통해 개별 숫자를 추출하고, 미리 저장된 템플릿과 비교하여 인식을 수행합니다.
5. ORB-SLAM2의 경우, 이는 실시간 단안 카메라 SLAM 시스템으로, ORB 특징점을 활용하여 카메라의 위치를 추적하고 3D 맵을 생성하는 시스템입니다. 이 시스템은 초기화, 트래킹, 로컬 매핑, 루프 클로징 등의 주요 모듈로 구성되어 있으며, 실시간으로 정확한 위치 추정과 맵 생성이 가능합니다. 학습 목적으로 이 시스템을 구현하고 분석하여 SLAM의 핵심 개념들을 이해하는데 중점을 두었습니다.

<br>
Code Repository: [GitHub](https://github.com/Harry-KIT){:target="_blank"}
{: .text-center}

</div>
