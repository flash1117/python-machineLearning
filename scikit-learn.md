- Feature , 속성

> Feature는 데이터 세트의 일반 속성.

머신러닝은 2차원 이상의 다차원 데이터에서도 많이 사용되므로 타겟값을 제외한 나머지 속성을 모두 Feature로 지칭.

- 레이블 , 클래스, 타겟 ( 값 ) , 결정 ( 값 )

> 타겟값 또는 결정값은 지도 학습 시 데이터의 학습을 위해 주어지는 정답 데이터.

지도 학습 중 분류의 경우에는 이 결정값을 레이블 또는 클래스로 지칭.

- 붓꽃 데이터 분류 예측 프로세스

1. 데이터 세트 분리 : 데이터를 학습 데이터와 테스트 데이터로 분리.

2. 모델 학습 : 학습 데이터를 기반으로 ML 알고리즘을 적용해 모델을 학습시킨다.

3. 예측 수행 : 학습된 ML 모델을 이용해 테스트 데이터의 분류 ( 붓꽃 종류 등 )을 예측한다.

4. 평가 : 이렇게 예측된 결과값과 테스트 데이터의 실제 결과값을 비교해 ML 모델 성능을 평가한다.

iris 내장 데이터셋을 로딩하는 함수

ML 결정트리를 사이킷런에서 구현한 것

학습데이터와 테스트 데이터를 원본데이터로 부터 분리시키는 함수로 구현 예정


Estimator - 사이킷런에서 부르는 이름

학습 : `fit()`
예측 : `predict()`

Classifier ( 분류 ) 구현 클래스

- DecisionTreeClassifier
- RandomForestClassifier
- GradientBoostingClassifier
- GaussianNB
- SVC

Regressor ( 회귀 ) 구현 클래스

- LinearRegression
- Ridge
- Lasso
- RandomForestRegressor
- GradientBoostingRegressor

Bunch 는 Python 의 dictionary와 비슷한 것. Key와 Value를 가지고 있다.

테스트데이터가 학습데이터랑 너무 비슷해버리면 결과가 좋게나와버리기 때문에 유의해야한다.
학습데이터에 없는데도 예측을 잘하는 알고리즘이 좋은 알고리즘이라고 할 수 있는 것.

## 교차 검증
