# Machine Learning Study

###### Summaries and References of ["Hands-On Machine Learning with Scikit-Learn and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems"](https://github.com/ageron/handson-ml) Book

## Chapter 1 - The Machine Learning Landscape

### 머신러닝이란 무엇인가?

- 컴퓨터 프로그래밍의 과학(및 예술)으로, 우리가 데이터에서 무언가를 배울 수 있게 해준다.

-- <cite>[Machine Learning is the] field of study that gives computers the ability to learn without being explicitly programmed. Arthur Samuel, 1959</cite>

-- <cite>A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E. Tom Mitchell, 1997</cite>

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

### 머신러닝 시스템의 종류

- 머신러닝 시스템을 분류하는 기준
    - 사람의 지도를 통한 교육을 받았는지의 여부에 따라 (지도 학습, 비지도 학습, 반지도 학습, 강화 학습)
    - 즉석에서 점진적으로 배울 수 있는지의 여부에 따라 (온라인 학습, 배치 학습)
    - 과학자들이 하는 것처럼 새로운 데이터 포인트를 알려진 데이터 포인트와 단순히 비교하거나 (인스턴스 기반 학습)
    - 트레이닝 데이터의 패턴을 감지하고 예측 모델을 작성해 작업하거나 (모델 기반 학습)

#### 지도 학습 / 비지도 학습

##### 지도 학습 (Supervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0105.png)

- 학습을 위해 알고리즘에 제공하는 트레이닝 데이터에 원하는 결과를 "레이블(Label)"로 달아둔다.

- 자주 사용하는 지도 학습 알고리즘
    - k-Nearest Neighbors
    - Linear Regression
    - Logistic Regression
    - Support Vector Machines (SVMs)
    - Decision Tree and Random Forests
    - Neural Networks

##### 비지도 학습 (Unsupervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0106.png)

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

##### 반지도 학습 (Semi-supervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0111.png)

- 지도 학습 + 비지도 학습 (레이블이 달린 데이터 약간, 레이블이 달리지 않은 데이터 대부분)

##### 강화 학습 (Reinforcement Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0112.png)

#### 배치 학습 / 온라인 학습

#### 인스턴스 기반 학습 / 모델 기반 학습

#### 머신 러닝의 주요 문제

### 테스트와 검증