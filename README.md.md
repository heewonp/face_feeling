# 멀티캠퍼스 세미프로젝트3

## 눈관상을 찾아라!

### CNN 이미지 분류 기반 `눈`관상 예측

1. 데이터 설명

   > 6가지 종류의 눈모양을 100~300 장 사이로 잘라낸 뒤, 증식

2. 데이터 전처리

   > opencv를 이용해 얼굴에서 눈 사진을 추출 한 뒤, 노이즈를 제거하고 특징을 부각시키기 위해 작업을 진행.
   >
   > ![image](https://user-images.githubusercontent.com/59459751/103170133-49be7180-4885-11eb-8954-3a2b95ac5cc7.png) 
   >
   > 하지만 전처리 없이 눈사진을 **직접** 추출해 그대로 사용하는것이 정확도가 더 높았음.

3. 알고리즘

   > 과적합을 방지하기 위해, batchnomerization, dropout을 각 층에 넣어 모델을 구성
   >
   > 마지막 층에서는 활성화 함수를 softmax로 설정하여 분류하고자 하는 눈 관상 종류인 6개로 나누어 출력
   >
   > ![image](https://user-images.githubusercontent.com/59459751/103170160-8b4f1c80-4885-11eb-8094-cae60ccd9fc2.png)

4. 모델링 결과

   > ![image](https://user-images.githubusercontent.com/59459751/103170177-a3bf3700-4885-11eb-9dfb-6073256db5eb.png)

5. 간단한 사이트 구성

   > 조코딩 유튜브를 참고하여 간략하게 구현, https://teachablemachine.withgoogle.com/ 사이트를 이용해 모은 눈사진을 넣어서 모델 구축 batch size =100, epochs=50으로 주고 학습시킴
   >
   > 메인페이지에서 사진을 올리면
   >
   > ![image](https://user-images.githubusercontent.com/59459751/103170289-9c4c5d80-4886-11eb-9459-ca390bcdb5c4.png)
   >
   > 결과가 사진처럼 나옴
   >
   > ![KakaoTalk_20201123_135639550](https://user-images.githubusercontent.com/59459751/103170268-76bf5400-4886-11eb-93f1-473465fdb78b.png)

6. 팀 구성 및 역할

   >공통: 이미지 데이터 수집, 모델링
   >
   >박희원  : 이미지 전처리, 결과발표, 웹사이트제작
   >
   >이동진 : 이미지 전처리
   >
   >이지윤: 발표 PT제작
   >
   >조원우 : 이미지 전처리