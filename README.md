# electric_predict
https://dacon.io/competitions/official/236125/overview/description

# 1. 개요

대회 기간은 끝났지만, 시계열 데이터를 다루는 머신러닝 프로젝트를 해보고 싶어 이 데이터를 이용해서 진행하였다. 
평소하던 머신러닝 뿐만 아니라 RNN기반의 딥러닝도 같이 사용하여 어느 쪽 성능이 더 좋게 나오는지도 실험해보고자 하였다.


<br />



# 2. 참여 인원 / 기간
* 개인 프로젝트
* 2023년 9월 16일 ~ 2023년 9월 24일


<br />


# 3. 사용 기술
* Python (Numpy, Pandas, Matplotlib, Seaborn)
* SQL
* Sklearn
* Pytorch


<br />


# 4. 분석 하고자 하는 대상



<br />


<details>
<summary>컬럼 설명</summary>


  

</details>

<br />



# 5. 분석 방법


  

<br />


# 6. 진행 과정


<br />


## 1. 전처리

첫번째 데이터셋은 시간별 날씨 (온도, 습도, 풍속 등)과 건물별 전력 사용량에 대한 데이터이다.
이 데이터에서 가장 중요한 점은 매 시간마다 날씨 데이터와 건물의 전력 사용량 데이터가 주어지는 시계열성 데이터라는 점이다. 
주어진 날짜에서 month, dow, day, hour를 따로 추출하여 새로운 컬럼으로 추가하였고, 추후 이 시간대별로 EDA를 진행하였다.

어떤 건물의 특정 시간대의 전력 사용량을 예측하기 위해, groupby를 이용해 건물별 시간별 전력 사용량의 평균과 표준편차의 새로운 피쳐를 생성해 데이터에 추가하였다. 또한, 시간 뿐만이 아니라 요일도 전력 사용량에 매우 큰 영향을 미칠 것이므로 건물별 요일별 전력 사용량의 평균과 표준편차도 추가하였다.
전력 사용량에 가장 큰 영향을 미치는건 냉난방에 관련된 요인일 것이고, 그 냉난방에 영향을 미치는건 온도와 습도도 있지만 불쾌지수가 가장 중요할 것이라고 생각하여 불쾌지수를 구하는 공식을 이용하여 새로운 컬럼을 추가하였다.

두번째 데이터셋은 건물들에 대한 데이터 (건물 유형, 냉방 면적, 기타 전력 용량 등)이다.
이 데이터에서는 


<br />


## 2. EDA

이 데이터에서 가장 중요한 점은 매 시간마다 날씨 데이터와 건물의 전력 사용량 데이터가 주어지는 시계열성 데이터라는 점이다. 건물별로 






<br />


## 3. 모델링
.


<br />


## 4. 예측


<br />


# 5. 회고 및 느낀점
