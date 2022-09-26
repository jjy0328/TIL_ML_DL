# 선형회귀 (linear regression)
  - 대표적 회귀 알고리즘
  - 비교적 간단하고 성능이 뛰어남

### 직선방정식

<img src = "https://drive.google.com/uc?id=1fu9ieZJAL8rvmqMx_LXxMkzMJtwsLu-R" height = 400 width = 500>

- 직선방정식의 a,b = lr객체의 coef_, intercept_
<br>
<br>
coef_ : 계수(coeifficient), 가중치(weight)
<br>
<br>

### 모델파라미터
- coef_, intercept_와 같이 ml 알고리즘이 찾은 값
-  ml 알고리즘의 훈련 과정 = 최적의 모델 파라미터 찾는 과정 <br>
=> **모델 기반 학습**
- 모델 파라미터가 없을 시, 훈련 세트를 저장하는 것이 훈련의 전부 <br>
=> **사례 기반 학습**


# 다항회귀

- 다항식을 이용한 선형회귀
- 선형회귀 그래프 : 일직선으로 뻗어있음 -> 0이하로 내려가는 직선 존재
- 산점도 : 왼쪽 위로 조금 구부러진 곡선<br>
<img src = "https://drive.google.com/uc?id=16oJ5GKNcqoGDOTihTrorVuORwesO1m7z" height = 400 width = 500><br><br>
=> **numpy를 이용하여 길이를 제곱한 항이 훈련 세트에 추가되어야 함**
