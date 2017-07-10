# Machine Learning Study

###### Summaries and References of ["Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems"](https://github.com/ageron/handson-ml) Book

## Chapter 1 - The Machine Learning Landscape

### 머신러닝이란 무엇인가?

- 컴퓨터 프로그래밍의 과학(및 예술)으로, 우리가 데이터에서 무언가를 학습할 수 있게 해준다.

<cite>[Machine Learning is the] field of study that gives computers the ability to learn without being explicitly programmed. Arthur Samuel, 1959</cite>

<cite>A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E. Tom Mitchell, 1997</cite>

### 왜 머신러닝을 사용하는가?

- 스팸 필터를 만드는 방법을 예로 들어 보자.

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0101.png)

- 기존 프로그래밍 기법
    - 스팸 메일로 판단할 수 있는 패턴을 찾아본다.
        - 대표적으로 단어나 구문이 있다. (예를 들어, "4U", "Credit Card", "Free", "Amazing" 등)
        - 또는 발신자 이름이나 발신자의 이메일 주소 등도 패턴이 될 수 있다.
    - 각 패턴에 대한 감지 알고리즘을 작성한다. 패턴이 많이 발견되면 해당 이메일을 스팸으로 분류한다.
    - 프로그램을 테스트하고, 좋은 결과가 나올 때까지 이전 단계를 반복한다.

- 기존 프로그래밍 기법은 문제가 자명하지 않을 경우, 복잡한 규칙으로 인해 프로그램을 유지 보수하기 어려워진다.

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0102.png)

- 머신러닝 기법
    - 스팸이 아닌 메일과 스팸이 아닌 메일 예제를 제공한다.
    - 두 예제를 비교해 스팸 메일로 판단할 수 있는 패턴을 자동으로 학습한다.

- 머신러닝 기법을 사용할 경우, 프로그램의 코드 길이는 더 짧아지고 정확도는 더 높아진다.

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0103.png)

- 스팸 메일을 보내는 사람들이 "4U"를 포함하는 메일이 막혔다는 사실을 알게 되었고, 대신 "For U"를 넣어 작성하기 시작했다고 하자.
    - 기존 프로그래밍 기법을 사용하는 스팸 필터는 "For U"를 포함하는 메일을 스팸으로 분류하기 위해 갱신해야 한다.
    - 스팸 메일을 보내는 사람들이 패턴을 바꿀 때마다, 새로운 규칙을 추가해야 한다. (어쩌면 영원히...)
    - 반면 머신러닝 기법을 사용하는 경우, 사용자들이 스팸이라고 표시한 메일에서 새로운 패턴인 "For U"를 자동으로 감지한다.
    - 따라서 여러분이 간섭하지 않아도, "For U"를 포함하는 메일을 스팸으로 분류하게 된다.
    
![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0104.png)
    
- 머신러닝 기법은 기존 프로그래밍 기법으로 해결하기에 너무 복잡하거나 알려진 알고리즘이 없는 문제에서 빛을 발한다.
    - "one"과 "two"를 구분하는 음성 인식 프로그램을 만든다고 하자.
    - 사람마다 음의 높이, 발음이 다르기 때문에 각 패턴에 대응하는 알고리즘을 만들기 쉽지 않다 (만들 수 있다고 하더라도 매우 복잡하다).
    - 가장 좋은 방법은 각 단어를 녹음한 수많은 예제를 주고, 스스로 학습해서 알고리즘을 만드는 머신러닝 기법을 사용하는 방법이다.
        - 수많은 데이터를 통해 바로 드러나지 않는 패턴을 발견하는 머신러닝 기법을 데이터 마이닝(Data Mining)이라고 한다.   

### 머신러닝 시스템의 종류

- 머신러닝 시스템을 분류하는 기준
    - 사람의 지도를 통한 교육을 받았는지의 여부에 따라 (지도 학습, 비지도 학습, 반지도 학습, 강화 학습)
    - 즉석에서 점진적으로 학습할 수 있는지의 여부에 따라 (온라인 학습, 배치 학습)
    - 과학자들이 하는 것처럼 새로운 데이터 포인트를 알려진 데이터 포인트와 단순히 비교하거나 (인스턴스 기반 학습)
    - 트레이닝 데이터의 패턴을 감지하고 예측 모델을 작성해 작업하거나 (모델 기반 학습)

#### 지도 학습 / 비지도 학습

##### 지도 학습 (Supervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0105.png)

- 학습을 위해 알고리즘에 제공하는 트레이닝 데이터에 원하는 결과를 "레이블(Label)"로 달아둔다.

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0106.png)

- 일반적으로 지도 학습을 많이 사용하는 작업
    - 분류 (Classification)
        - 스팸 필터를 예로 들어보자.
        - 스팸 필터는 종류(Class)를 표시해 놓은 수많은 이메일 예제를 통해 새 메일을 어떻게 분류할 지 학습한다.
    - 회귀 (Regression)
        - 예측 변수(Predictor)라고 하는 특징(Feature) 집합(주행 거리, 연식, 브랜드 등)을 통해 대상(Target) 값(중고차의 가격)을 예측한다.
        - 시스템을 학습시키려면, 수많은 중고차 예제를 준비해야 한다. 각 예제에는 예측 변수와 레이블(중고차의 가격)이 있어야 한다.
    - 분류와 회귀를 혼합해서 사용하기도 한다.
        - 로지스틱 회귀(Logistic Regression)는 일반적으로 분류에서 사용하는데, 주어진 종류로 분류될 확률을 값으로 알려준다.
        - 예를 들어, 스팸 필터라면 "스팸 메일일 확률은 20%"라고 알려준다. 
  
- 자주 사용하는 지도 학습 알고리즘
    - k-Nearest Neighbors
    - Linear Regression
    - Logistic Regression
    - Support Vector Machines (SVMs)
    - Decision Tree and Random Forests
    - Neural Networks

##### 비지도 학습 (Unsupervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0107.png)

- 학습을 위해 알고리즘에 제공되는 트레이닝 데이터에 레이블을 달아두지 않는다.

- 자주 사용하는 비지도 학습 알고리즘
    - Hierarchical Cluster Analysis (HCA)
    - Expectation Maximization
    - Visualization and Dimensionality Reduction
    - Principal Component Analysis (PCA)
    - Kernel PCA
    - Locally-Linear Embedding (LLE)
    - t-distributed Stochastic Neighbor Embedding (t-SNE)
    - Association rule learning
    - Apriori
    - Eclat
    
![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0108.png)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0109.png)
    
- 일반적으로 비지도 학습을 많이 사용하는 작업
    - 군집화 (Clustering)
        - 여러분의 블로그 방문자들을 예로 들어보자.
        - 군집화 알고리즘을 사용해 비슷한 방문자들을 그룹으로 만들 수 있다.
        - 예를 들어, 방문자의 40%가 만화책을 좋아하며 저녁에 블로그 글을 읽는 남자라는 사실을 알 수 있다.
        - 또한 방문자의 20%가 SF를 좋아하며 주말에 블로그 글을 읽는 20대라는 사실도 알 수 있다.
        - 만약 계층적 군집화(Hierarchical Clustering) 알고리즘을 사용한다면, 각 그룹을 더 작은 그룹으로 나눌 수 있다.
        - 이를 통해 각 그룹에 특화된 블로그 게시물을 작성할 수 있다.
    - 시각화 (Visualization)
        - 엄청난 수의 레이블이 달려있지 않은 복잡한 데이터를 분석해야 할 때 유용하다.
        - 입력받은 데이터를 분석해 2D나 3D로 시각화한다.
        - 데이터가 어떻게 구조화되는지 이해하고, 그리고 예상치 못한 패턴을 찾는데 도움이 된다. 
        - 차원 감소 (Dimensionality Reduction)
            - 많은 정보를 잃지 않으면서 데이터를 단순화하는 기법
            - 연관되어 있는 여러 특징들을 하나로 합치는 방법을 사용한다.
            - 예를 들어, 중고차의 주행 거리는 연식과 매우 연관되어 있다.
            - 따라서, 차원 감소 알고리즘을 통해 하나의 특징(마모)으로 합칠 수 있다. 이를 특징 추출(Feature Extraction)이라고 한다.
    - 이상 감지 (Anomaly Detection)
        - 예를 들어, 사기를 방지하기 위해 비정상적인 신용 카드 거래를 탐지하거나 제조 결함을 감지하는데 사용할 수 있다.
        - 다른 학습 알고리즘에 제공하지 전에 데이터 집합에서 특이점을 자동으로 제거한다.
        - 시스템이 정상적인 인스턴스로 학습했다면, 새로운 인스턴스가 들어왔을 때 정상적인 인스턴스인지의 여부를 알 수 있다.
    - 연관 규칙 학습 (Association Rule Learning)
        - 수많은 데이터를 파헤쳐 속성 간의 흥미로운 관계를 발견하는데 사용할 수 있다.
        - 예를 들어, 슈퍼마켓 가게를 하나 갖고 있다고 가정하자.
        - 영업 기록에 연관 규칙을 적용하면 바베큐 소스와 감자 칩을 구입하는 사람들이 스테이크도 구입하는 경향이 있다는 점을 알 수 있다.
        - 따라서 이 제품들을 서로 가깝게 배치해 매출을 올릴 수 있다.

##### 반지도 학습 (Semi-supervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0111.png)

- 지도 학습 + 비지도 학습 (레이블이 달린 데이터 약간, 레이블이 달리지 않은 데이터 대부분)

- 예제 : Google Photos
    - 여러분이 11장의 사진을 업로드했다고 하자.
    - Google Photos 서비스는 A라는 사람이 1, 5, 11번, 그리고 B라는 사람이 2, 5, 7번 사진에 등장했다는 사실을 자동으로 인지한다.
    - 이는 알고리즘의 비지도 부분(군집화)이라고 할 수 있다.
    - 이제 여러분은 이 사람이 누군지 시스템에 알려줘야 한다.
    - 사람마다 레이블을 한 번만 달아주면, 모든 사진에 등장하는 해당 인물에 이름이 지정되므로 검색할 때 유용하다.

- 일반적으로 반지도 학습을 많이 사용하는 작업
    - 심층 신뢰 신경망 (Deep Belief Network; DBN)
        - 비지도 구성 요소인 제한된 볼츠만 기계(Restricted Boltzmann Machine; RBM)를 기반으로 한다.
        - RBM은 비지도 학습 방식을 통해 순차적으로 트레이닝되고, 시스템 전체는 지도 학습 방식을 사용해 미세하게 조정한다.

##### 강화 학습 (Reinforcement Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0112.png)

- 앞에서 소개했던 세 가지 학습 방법과는 많이 다른 학습 방법이다.
    - 에이전트(Agent)라고 하는 학습 시스템은 환경을 관찰하고, 행동을 선택하고 수행하며, 결과로 보상(Reward)이나 패널티(Panelty)를 받는다.
    - 시간이 지남에 따라 정책(Policy)이라고 하는 가장 많은 보상을 얻기 위한 최상의 전략을 스스로 학습한다.
    - 정책은 주어진 상황에서 선택해야 하는 행동을 정의한다.
    - 예를 들어, 많은 로봇이 도보 학습 방법을 배우려고 강화 학습 알고리즘을 구현한다.

- DeepMind의 AlphaGo 프로그램은 강화 학습의 좋은 예다.
    - 수백만 게임을 분석한 다음, 자체적으로 여러 게임을 실행해 성공적인 정책을 학습했다.
    - 바둑 기사들을 상대로 게임을 하는 동안, 강화 학습은 꺼져 있었다.
    - AlphaGo는 스스로 학습한 정책을 적용하고 있었을 뿐이다.

#### 배치 학습 / 온라인 학습

##### 배치 학습 (Batch Learning)

- 시스템은 점진적으로 학습할 수 없으며, 모든 사용 가능한 데이터를 사용해 학습해야 한다.
    - 많은 시간과 컴퓨터 자원이 필요하므로, 일반적으로 오프라인으로 수행한다.
    - 시스템이 학습하고 나면, 생산 단계로 넘어가 더 이상 학습하지 않고 실행된다.
    - 이런 이유로 오프라인 학습(Offline Learning)이라고 부르기도 한다.

- 새로운 데이터에 대해 알고 싶다면, 전체 데이터 집합(기존 데이터 + 새 데이터)을 처음부터 다시 학습해야 한다.
    - 다행스럽게도, 머신러닝 시스템의 학습/계산/실행 과정은 쉽게 자동화 할 수 있다.
    - 하지만 전체 데이터 집합을 학습하는데 많은 시간이 걸릴 수 있으므로 보통 24시간 주기로 수행한다.
    - 또한 컴퓨터 자원(CPU, 메모리 공간, 디스크 공간, 디스크 I/O, 네트워크 I/O)이 많이 필요하다.
    - 이로 인해 비용이 많이 들며, 데이터 집합이 기하급수적으로 커지면 배치 학습 알고리즘 사용이 불가능해 질 수도 있다.
    - 보다 나은 방법으로, 점진적으로 학습할 수 있는 알고리즘을 사용하는 방법이 있다.

##### 온라인 학습 (Online Learning)

#### 인스턴스 기반 학습 / 모델 기반 학습

##### 인스턴스 기반 학습 (Instance-based Learning)

##### 모델 기반 학습 (Model-based Learning)

#### 머신 러닝의 주요 문제

##### 트레이닝 데이터의 수가 불충분한 문제

##### 대표성을 띄지 않는 트레이닝 데이터

##### 저품질의 데이터

##### 무관한 특징

##### 트레이닝 데이터의 과적합 (Overfitting)

##### 트레이닝 데이터의 과소적합 (Underfitting)

### 테스트와 검증
