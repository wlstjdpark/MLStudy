# 머신 러닝을 위한 수학

## 선형 대수

''V''를 [[체 (수학)|체]] <math>F\;(F=\mathbb{R}\text{ or }\mathbb{C})</math> 위에 주어진 [[벡터공간]]이라고 하자. [[함수 (수학)|함수]] <math>(\cdot,\cdot):V\times V\to F</math>가 임의의 <math>\mathbf{x},\mathbf{y},\mathbf{z}\in V</math>와 <math>c\in F</math>에 대해
: (1) <math>(\mathbf{x},\mathbf{x})\ge 0</math>
: (1a) <math>(\mathbf{x},\mathbf{x})=0 \Leftrightarrow \mathbf{x}=0</math>
: (2) <math>(\mathbf{x}+\mathbf{y},\mathbf{z})=(\mathbf{x},\mathbf{z})+(\mathbf{y},\mathbf{z})</math>
: (3) <math>(c\mathbf{x},\mathbf{y})=c(\mathbf{x},\mathbf{y})</math>
: (4) <math>(\mathbf{x},\mathbf{y})=\overline{(\mathbf{y},\mathbf{x})}</math>
을 만족하면 <math>(\cdot,\cdot)</math>를 '''내적(inner product)'''이라고 한다. 만약 벡터공간에 내적이 주어져 있으면 '''내적공간(inner product space)'''이라고 한다.

### 벡터 공간

- 원소를 서로 더하거나, 주어진 배수로 늘이거나 줄일 수 있는 공간이다.
- 벡터 공간 는 다음을 만족한다.
    - 덧셈에 대한 항등원 존재 : 에는 특정한 원소 0이 존재해 모든 에 대해
    - 덧셈에 대한 역원 존재 : 의 임의의 원소 에 대해 을 만족하는 가 존재한다.
    - 곱셈에 대한 항등원 존재 : 에는 특정한 원소 1이 존재해 모든 에 대해
    - 교환법칙 성립 : 
    - 결합법칙 성립 : 
    - 분패법칙 성립 : 

#### 유클리드 공간

### 거리 공간

- 를 집합이라 하고 를 에서 0 이상을 갖는 실수의 집합 로의 함수라고 하자. 임의의 에 대해, 다음 조건을 만족하면 를 위의 거리(Metric), 또는 거리 함수(Distance Function)라고 한다.
- 그리고 를 에서 까지의 거리(Distance)라고 한다.
- 거리 함수 가 주어진 집합 를 거리 공간(Metric Space)라고 하고 라고 표기한다.
- 참고로 영어 단어 Metric과 Distance는 모두 "거리"라고 번역하는데, 엄밀하게 따지면
    - Distance는 거리 값을 나타내는 스칼라를 말한다.
    - Metric은 미분기하학적 측면에서 텐서를 말한다.

### 노름 공간

- 를 체 위에서 정의된 벡터 공간이라고 하자. 함수 가 임의의 와 임의의 에 대해, 다음 조건을 만족하면 노름(Norm)이라고 한다.
- 노름이 주어지는 벡터 공간을 노름 공간(Norm Space)이라고 한다.

### 내적 공간

- 를 체 위에 주어진 벡터 공간이라고 하자. 함수 가 임의의 와 에 대해, 다음 조건을 만족하면 를 내적(Inner Product)이라고 한다.
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D%5C%7C%5Cge%200)
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%20c%5Cmathbf%7Bx%7D%5C%7C%3D%7Cc%7C%5C%7C%5Cmathbf%7Bx%7D%5C%7C)
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D&plus;%5Cmathbf%7By%7D%5C%7C%5Cle%20%5C%7C%5Cmathbf%7Bx%7D%5C%7C&plus;%5C%7C%5Cmathbf%7By%7D%5C%7C)
- 만약 벡터 공간에 내적이 주어져 있으면, 내적 공간(Inner Product Space)이라고 한다.

### 치환

### 고유한 것들

### 대각합

### 행렬식

### 특별한 종류의 행렬

### 특이값 분해

## 미분/적분과 최적화

### 극값

### 그래디언트

### 헤시안

### 테일러 정리

### 볼록성

## 확률

### 기초

#### 조건부 확률

#### 연쇄 법칙

#### 베이즈 정리

### 확률 변수

#### 이산 확률 변수

#### 연속 확률 변수

#### 누적 분포 함수

### 결합 분포

#### 확률 변수의 독립

#### 주변 분포

### 기댓값

#### 기댓값의 성질

### 분산

#### 분산의 성질

### 공분산

#### 상관 관계

### 확률 벡터

### 매개 변수의 추정

#### 최대 우도

#### 최대 사후 확률