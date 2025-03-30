---
layout: post
modalID: modalUdacityLaneLineDetection1
permalink: /:categories/:slug/
main_title: 미스트랄 파인튜닝

thumb_image_url: assets/post_assets/udacity-lane-line-detection-1/images/original/mistral_demo.png

category: projects
project_title: "미스트랄 파인튜닝"
thumb_text: 미스트랄 파인튜닝
tech:
  - LLMs

---

<div class="post-content-markdown">


저는 Databricks Dolly-15k 데이터세트로 Mistral 미세 조정을 다시 구현했습니다. 저의 접근 방식은 4비트 양자화와 LoRA를 사용하여 소비자 하드웨어에서도 이 7B 매개변수 모델을 미세 조정할 수 있도록 합니다.
파이프라인은 Mistral-7B를 로드하고 4비트 정밀도로 양자화하고 랭크 8의 학습 가능한 LoRA 어댑터를 추가합니다. 데이터세트의 경우 적절한 프롬프트 템플릿과 함께 Dolly의 명령어 추종 형식을 사용합니다.
학습 루프에는 그래디언트 축적(1개의 배치이지만 2단계 동안 축적), 워밍업이 있는 코사인 학습률 일정, 주기적 검증이 포함됩니다. 전체 설정은 여전히 ​​좋은 미세 조정 결과를 생성하는 동시에 메모리 효율적이도록 설계되었습니다.
{: .text-left}

## 주요 구현 세부 정보:

* 양자화: 이중 양자화를 사용한 4비트 NF4 형식
* LoRA 매개변수: r=8, 알파=16, 드롭아웃=0.05
* 훈련: 학습률 3e-5로 1에포크
* 시퀀스 길이는 메모리에 맞게 380개 토큰으로 제한됨

Code Repository: [GitHub](https://github.com/Harry-KIT){:target="_blank"}
{: .text-center}

</div>
