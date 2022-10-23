# 다중 회귀
- 여러 개의 특성을 사용한 선형회귀
- 타깃 = (a * 특성1) + (b * 특성2) + 절편
- 특성이 많은 고차원에서는 선형 회귀가 매우 복잡한 모델 표현 가능


## 특성공학
- 기존의 특성을 사용하여 새로운 특성을 뽑아냄


## 사이킷런 변환기
- 전처리를 하기 위한 다양한 클래스 제공
- fit(), transform() 메소드 제공
- 각 특성을 제곱한 항, 특성끼리 서로 곱한 항 , 1 (절편을 1인 특성과 곱해지는 계수로 봄) 추가

---

# 규제 (Regularization)

- 훈련세트를 과도하게 학습하지 못하도록 훼방
- 모델이 훈련 세트에 과대적합하지 않도록 만들어줌
- 선형 회궤 모델의 경우 특성에 곱해지는 계수의 크기를 작게 만드는 일


## 릿지(Ridge)
- 선형 회귀 모델에 규제를 추가한 모델
- **계수를 제곱한 값을 기준으로 규제 적용**
- 선형 모덿의 계수를 작게 만들어 과대적합을 완화
- 비교적 효과가 좋아 자주 사용하는 모델

## 라쏘(Lasso)
- 선형 회귀 모델에 규제를 추가한 모델
- **계수의 절댓값 기준**
- 계수의 크기를 0으로 만들 수 있음
- lasso 모델 훈련 시 : `convertgenceWarning`
    - 최적의 계수를 찾기 위해 반복적인 계산 수행 -> 지정한 반복 횟수가 부족할 때 생기는 경고


## alpha값

- alpha 매개변수로 모델의 값 규제
- alpha값이 오름 -> 규제 강도가 세짐 -> 과소적합 유도
- alpha 값이 내림 -> 규제 강도가 낮아짐 -> 과대적합 유도
- 적절한 값을 찾기 위해 결정계수의 그래프 그려보기
- 테스트와 훈련 세트가 가장 가까운 지점 = 최적의 alpha 값