---
layout: post
modalID: modalUdacityCarndPathPlanning
permalink: /:categories/:slug/
main_title: 시뮬레이션 자동차의 경로 계획

thumb_image_url: assets/post_assets/udacity-path-planning/videos/webm/react-to-other-change.webm
images:
  - {
    url: "assets/post_assets/udacity-path-planning/videos/gif/react-to-other-change.gif",
    id: "react-to-other-change"
  }
  - {
    url: "assets/post_assets/udacity-path-planning/videos/gif/double-lane-change.gif",
    id: "double-lane-change"
  }
  - {
    url: "assets/post_assets/udacity-path-planning/images/compressed/sd-path-zoomed.png",
    caption: "On a straight road, this is what kind of s,d coordinates getFrenet sometimes returns, hence the difficulties I've had.",
    id: "sd-path-zoomed"
  }
category: projects
project_title: "시뮬레이션 자동차의 경로 계획"
thumb_text: 시뮬레이션 자동차의 경로 계획.
tech:
  - Planning
  - C++
size: large
unlisted: false

---

<div class="post-content-markdown">

시뮬레이터에 오류가 있는 자율주행차 경로 계획 프로젝트입니다. 이 프로젝트는 3개 차선에서 다른 차량들을 고려하면서 차량의 최적 경로를 계획하는 것이 목표였습니다. 개발 과정에서 시뮬레이터의 프레넷 좌표계 변환(Frenet Coordinate transformation) 오류와 속도 측정 오류라는 두 가지 중요한 문제점이 발견되었습니다. 이러한 문제들을 해결하기 위해 스플라인(spline) 라이브러리를 활용하여 경로를 생성하고, 차량의 실제 속도를 독립적으로 계산하는 방식을 도입했습니다. 결과적으로 차선 변경이 필요할 때 안전하게 변경하면서도 속도 제한을 준수하는 안정적인 주행 시스템을 구현하는 데 성공했습니다.

<br>

Code Repository: [GitHub](https://github.com/Harry-KIT/CarND-Path-Planning-Project){:target="_blank"}
{: .text-center}

</div>
