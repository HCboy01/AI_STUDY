
## 머신러닝 (machine learning)
------
## 1 - 1 머신러닝 이란?

- 일반적인 정의
```
머신러닝은 명시적인 프로그래밍 없이 컴퓨터가 학습하는 능력을 갖추게 하는 연구분야이다.
_아서 새뮤얼, 1959
```

- 공학적인 정의
```
어떤 작업 T에 대한 컴퓨터 프로그램의 성능을 P로 측정했을 때 경험 E로 인해 성능이 향상되었다면, 이 컴퓨터 프로그램은 작업 T와 성능 측정 P에 대해 경험 E로 학습했다고 할 수 있다.
- 톰 미첼
```

---
## 1 - 2 왜 머신러닝을 사용하는가?

1. 유지보수 문제
- 어떤 복잡한 문제에 대해 기존의 프로그래밍 방식을 통해 문제를 해결한다면, 복잡하고 긴 규칙을 적용해야만 할 것이고, 때문에 변화에 대응하기가 어려워 유지보수가 힘들어질 것이다.
- 머신러닝 기법에 기반을 둔 프로그램은 데이터에 자주 나타나는 패턴을 스스로 학습하기 때문에, 유지보수하기가 쉬우며 대부분의 경우에서 정확도도 높다.

2. 혁신적인 해결
- 기존의 방법으로는 해결할 수 없었던 문제 (예를 들어 음성인식, 정교한 규칙으로 one과 two를 구분할 수 는 있겠지만 수백만명이 말하는 수천개의 언어를 커버할 수는 없을 것이다.)의 해결법이 될 수 있다.

3. 데이터 마이닝
- 머신러닝 알고리즘이 학습한 것을 역으로 조사하여 데이터들 사이에서의 예측하지 못했던 연관관계등을 얻어낼 수 있다.

---
## 1 - 3 애플리케이션 사례
---

// 책에 나와있고 무슨 이론이 쓰였는지는 지금 써도 모르기 때문에 간단히 작성
- 생산 라인에서의 이미지 분류
- 뇌를 스캔해서 종양 진단
- 뉴스 기사 분류
- 부정적인 텍스트 처리
- 긴 문서 요약
- 챗봇
- 성능 지표를 기반으로 회사의 내년 수익을 예측
- 음성 인식
- 부정 거래 감지
- 구매 이력에 따른 고객별 맞춤 마케팅
- 고차원의 데이터 셋을 의미있는 그래프로 변환
- 상품 맞춤 추천
- 지능형 게임 봇 (알파고)

등등...에서 다양하게 활용되고 있다

---
## 1 - 4 머신러닝 시스템의 종류
---

- 지도, 비지도, 준지도, 강화 학습 (사람의 관리감독 여부에 따라)
- 온라인, 배치 학습 (실시간으로 학습이 이루어지는지?)
- 사례 기반, 모델 기반 학습 (단순히 알고 있는 데이터와의 비교인지, 데이터 셋에서 패턴을 발견하여 예측하는지)

### 1 - 4 - 1 지도 학습과 비지도 학습
---
#### 지도학습

- 알고리즘에 주입하는 훈련 데이터에 레이블 (출력하고자 하는 답)이 포함된다.
- 분류 와 회귀 알고리즘에 주로 활용된다.
##### 분류
- 훈련 결과를 바탕으로 주어진 데이터가 레이블에 해당하는지 아닌지 판별하는 작업
##### 회귀
- 훈련 결과를 바탕으로 주어진 데이터가 가질 타깃 수치를 예측하는 것

##### 주로 사용하는 지도학습 알고리즘
- k-최근접 이웃 (k-nearest neighbors)
- 선형 회귀 (linear regression)
- 로지스틱 회귀 (logistic regression)
- 서포트 벡터 머신 (support vector machine) (SVM)
- 결정 트리 (decision tree), 랜덤 포레스트 (random forest)
- 신경망 (neural networks)

---
#### 비지도 학습

- 훈련 데이터에 레이블이 없음
- 군집, 이상치 탐지와 특이치 탐지, 시각화와 차원 축소, 연관 규칙 학습 알고리즘 등에 사용된다.

##### 군집
- 그룹을 특성에 따라 알고리즘이 스스로 세분화 하여 분류한다.
- 이를 이용하여 각 그룹에 맞는 행동을 취하는 것이 가능하다.

##### 시각화
- 레이블이 없는 대규모의 데이터를 분석하여 2D 혹은 3D의 도식화 가능한 표현을 만들어준다.
- 이를 통해 데이터를 이해하고, 패턴을 찾을 수도 있다.

##### 차원 축소
- 상관관계가 있는 여러 특성을 찾아 하나로 합치는 것 (특성 추출)
- 너무 많은 정보를 잃지 않으면서 규모를 줄일 수 있다.

##### 이상치 탐지
- 훈련하는 동안 정상 데이터를 이용하여 훈련하고, 이후 새로운 샘플을 보고 정상인지 이상치인지를 판단하는 것

##### 특이치 탐지
- 훈련 세트의 모든 샘플과 달라보이는 새로운 샘플인지 판별하는 것
- 매우 깨끗한 훈련 세트가 요구됨.

##### 연관 규칙 학습
- 대량의 데이터를 군집화 하면서, 특성간의 연관관계를 찾아내는 것 (ex: 슈퍼마켓 판매기록을 분석하여 스테이크를 사는 사람들이 양념도 많이 산다는 연관관계를 도출)


---
#### 준지도 학습

- 지도 학습 + 비지도 학습

##### 심층 신뢰 신경망 (deep belief network) (DBN)
- 여러겹으로 쌓인 제한된 볼츠만 머신 (비지도 학습)에 기초
- 비지도 학습으로 훈련된 데이터를 지도학습 방식으로 세밀하게 조정하는 식


---
#### 강화 학습
- 위 학습들과는 다른 결의 학습 방법
- 학습하는 시스템을 에이전트라 하고 환경을 관찰하여 행동했을 때의 결과를 보상(reward)과 벌점(penalty)로 구분한다.
- 시간이 지나면 시스템은 가장 큰 보상을 받기 위한 정책(policy)이라 불리는 최상위 전략을 스스로 학습한다.
- 알파고 ! !


---

### 1 - 4 - 2 배치 학습과 온라인 학습

- 입력 데이터의 스트림으로부터 점진적으로 학습할 수 있는지를 기준으로 나눔
---
#### 배치 학습
- 점진적으로 학습하지 못하는 알고리즘. 학습 -> 적용의 반복
- 오프라인 학습 (오프라인에서 훈련하고, 적용하니까)

- 변화에 대응하기 위해 전체 데이터셋으로 다시 훈련해야 하므로, 빠른 대응을 요하는 작업에 비효율적
- 데이터 셋이 커진다면 점점 더 많은 컴퓨팅 자원과 시간이 필요할 것.
- 자원이 제한된 시스템의 경우 제한될 수 있다.
---
#### 온라인 학습
- 데이터를 한개 또는 작은 미니 배치로 나누어 시스템을 훈련
- 매 학습 단계가 금방 끝나므로 연속적으로 학습이 가능

- 빠른 변화에 대응하기 용이하다.
- 컴퓨팅 자원이 제한 된 경우에도 활용 가능하다 (학습한건 버리면 되니까)

- 아주 큰 데이터를 학습하는 경우에도 알고리즘이 데이터의 일부를 훈련하며 진행하는 방식의 외부 데이터 학습 을 차용할 수 있다. (이 경우는 오프라인 학습이지만, 점진적 학습이다.)

##### 학습률
- 온라인 학습에서 새로운 데이터에 얼마나 빠르게 적응할 것인지를 결정하는 파라미터
- 학습률이 높으면 이전 학습한 데이터를 금방 잊어버릴 것이다.
- 학습률이 낮으면 새로운 데이터에 대한 적응이 늦어질 것이다.

##### 온라인 학습의 단점
- 나쁜 데이터에 장기적으로 노출되었을때 시스템이 손상될 수 있다.
	-> 면밀한 모니터링과 이상치 탐지 알고리즘 등으로 나쁜 데이터를 걸러내야 한다.

---

### 1 - 4 - 3 사례 기반 학습과 모델 기반 학습
- 어떤 방식으로 일반화 하는가(어떻게 새로운 데이터를 예측하는가)를 기준으로 분류

#### 사례 기반 학습
- 단순히 학습한 데이터를 기억하는 것
- 기억한 데이터를 기반으로 새로운 데이터 사이의 유사도를 측정

#### 모델 기반 학습
- 샘플들의 모델을 만들어 예측 하는 것
- ex) 선형 모델
		어떤 데이터들이 선형적인 경향을 띠는 것으로 나타났다면 이를 선형 모델로 계산
		y = a + b * x 와 같은 형태 (a, b는 모델 파라미터)

##### 파라미터는 어떻게 정의하나?
- 모델이 얼마나 좋은지를 측정하는 효용 함수 (적합도 함수) 를 측정하거나
- 모델이 얼마나 나쁜지를 측정하는 비용 함수를 정의하여 측정한다.

데이터를 공급했을 때 가장 적합한 파라미터를 찾는 과정을 훈련한다고 한다!

---

## 1 - 5 머신러닝의 주요 도전 과제
---
- 머신러닝을 공부하면서 부딪히게 되는 주요 문제는 크게 "나쁜 알고리즘"과 "나쁜 데이터"가 있다.

### 1 - 5 - 1 충분하지 않은 양의 훈련 데이터
---
- 어린아이에게 사과에 대해 인지하게 하려면 여러개의 예시만 있으면 되지만, 머신러닝 알고리즘에게는 아직 많은 데이터가 필요하다.
- 복잡한 문제에 있어서 대부분은 알고리즘보다 데이터의 양이 정확도에 더 큰 영향을 미치기도 한다.
- 하지만 많은 데이터를 확보하는 것이 쉬운일은 아니므로, 충분한 데이터를 확보하되 알고리즘 또한 무시해서는 안될 것이다!
### 1 - 5 - 2 대표성 없는 훈련 데이터
---
- 훈련세트가 잘 정제되어 있는가? 를 따지는 문제.
- 훈련 세트가 일반화 하려는 사례를 잘 대표하고 있는가를 따져봐야 한다.
- 데이터가 충분치 않다면 샘플링 잡음(우연히 대표성 없는 훈련세트가 됨)이 생길 수 있고,
- 데이터 수집 방식이 잘못되었다면 샘플링 편향이 있을 수 있어 주의해야 한다.

### 1 - 5 - 3 낮은 품질의 데이터
---
- 데이터의 정제가 필요한 경우
	- 일부 샘플이 이상치인 것이 명확한 경우 걸러줘야 함.
	- 일부 샘플에 특성이 온전치 않다면 특성을 무시할지, 해당 샘플들을 무시할지 등을 결정해야 함.

### 1 - 5 - 4 관련 없는 특성
---
- 훈련 데이터와 관련이 있는 특성을 잘 골라야 한다. (garbage in, garbage out!)
- 특성 선택: 가지고 있는 특성 중 유용한 특성을 선택하는 것
- 특성 추출: 특성들을 결합하여 더 유용한 특성을 만드는 것
- 이러한 과정을 특성 공학 이라 부른다.

### 1 - 5 - 5 훈련 데이터 과대적합
---
- 훈련 모델이 지나치게 데이터에 잘 맞는 경우 오히려 일반화에 실패할 수 있다 ...
- 복잡한 모델은 데이터가 충분치 않을 경우 데이터에서 잡음이 섞인 패턴을 발견 할 수 있다.

##### 과대 적합 해결 방법
- 파라미터의 수가 적은 모델 선택하기, 특성 수를 줄이거나 모델에 제약을 걸어서 단순화하기.
- 훈련 데이터를 더 많이 모으기
- 데이터의 잡음 줄이기

##### 규제
- 모델을 단순화 하기 위해 제약을 가하는 것.
- 규제의 양은 하이퍼 파라미터가 결정한다.
- 훈련 데이터에 완벽히 맞추는 것과, 일반화를 위해 단순함을 유지하는 것중 균형을 맞출 필요가 있다.

### 1 - 5 - 6 훈련 데이터 과소적합
---
- 모델이 너무 단순해서 일반화에 실패하는 경우

##### 과소 적합 해결 방법
- 모델 파라미터가 더 많은 모델 선택하기
- 더 좋은 특성 선택하기
- 모델의 제약 줄이기


## 1 - 6 테스트와 검증
---
- 훈련을 마친 모델을 검증하지 않고 내놓을 수는 없기 때문에 보통 훈련데이터를 훈련 세트와 테스트 세트 두 개로 나눈다.
- 보통 8:2의 비율로 나누지만 데이터의 양이 충분히 많은 경우에는 그렇게까지 많은 테스트 세트가 필요하지는 않다.
- 테스트 세트에서의 오류 비율을 일반화 오차 (외부 샘플 오차) 라고 하는데, 훈련 오차는 적지만 일반화 오차가 큰 경우 과대적합되었다고 할 수 있다.

### 테스트 세트 활용의 문제
- 하이퍼 파라미터값을 조정해가면서 일반화 오차가 가장 낮은 모델을 선택했다고 할때, 모델이 완벽하게 일반화되었다고 보기는 어렵다.
- 여러 하이퍼 파라미터 값에 따른 모델을 비교하면서, 모델이 테스트 세트에 최적화 된 상태이기 때문이다.

### 홀드아웃 검증
- 훈련 세트의 일부를 떼어내어 검증 세트로 만들고
- 검증 세트를 뺀 훈련 세트의 파라미터 값을 조정하여 검증 세트에서 최고의 효율을 내는 모델을 선택한다.
- 해당 모델로 전체를 다시 훈련하고 일반화 오차를 측정한다.
- 교차 검증을 통해 정확도를 높일 수 있다. (다양한 검증세트로 훈련)
