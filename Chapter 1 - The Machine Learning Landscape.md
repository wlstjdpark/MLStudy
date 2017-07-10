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

##### 반지도 학습 (Semi-supervised Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0111.png)

- 지도 학습 + 비지도 학습 (레이블이 달린 데이터 약간, 레이블이 달리지 않은 데이터 대부분)

##### 강화 학습 (Reinforcement Learning)

![](https://github.com/utilForever/MLStudy/blob/master/Resources/mlst_0112.png)

#### 배치 학습 / 온라인 학습

#### 인스턴스 기반 학습 / 모델 기반 학습

#### 머신 러닝의 주요 문제

### 테스트와 검증
