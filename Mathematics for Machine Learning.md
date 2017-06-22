# 머신 러닝을 위한 수학

## 선형 대수

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

- ![](http://latex.codecogs.com/gif.latex?%5C%28X%5C%29)를 집합이라 하고 ![](http://latex.codecogs.com/gif.latex?%5C%28d%5C%29)를 ![](http://latex.codecogs.com/gif.latex?X%5Ctimes%20X)에서 0 이상을 갖는 실수의 집합 ![](http://latex.codecogs.com/gif.latex?%5Cmathbb%7BR%7D%5E&plus;)로의 함수라고 하자. 임의의 ![](http://latex.codecogs.com/gif.latex?x%2Cy%2Cz%5Cin%20X)에 대해, 다음 조건을 만족하면 ![](http://latex.codecogs.com/gif.latex?d%3AX%5Ctimes%20X%5Cto%20%5Cmathbb%7BR%7D%5E&plus;)를 ![](http://latex.codecogs.com/gif.latex?X) 위의 거리(Metric), 또는 거리 함수(Distance Function)라고 한다.
    - ![](http://latex.codecogs.com/gif.latex?d%28x%2Cy%29%3D0%20%5CLeftrightarrow%20x%3Dy)
    - ![](http://latex.codecogs.com/gif.latex?d%28x%2Cy%29%3Dd%28y%2Cx%29)
    - ![](http://latex.codecogs.com/gif.latex?d%28x%2Cz%29%5Cle%20d%28x%2Cy%29&plus;d%28y%2Cz%29)
- 그리고 ![](http://latex.codecogs.com/gif.latex?d%28x%2Cy%29)를 ![](http://latex.codecogs.com/gif.latex?x)에서 ![](http://latex.codecogs.com/gif.latex?y)까지의 거리(Distance)라고 한다.
- 거리 함수 ![](http://latex.codecogs.com/gif.latex?d)가 주어진 집합 ![](http://latex.codecogs.com/gif.latex?X)를 거리 공간(Metric Space)라고 하고 ![](http://latex.codecogs.com/gif.latex?%28X%2Cd%29)라고 표기한다.
- 참고로 영어 단어 Metric과 Distance는 모두 "거리"라고 번역하는데, 엄밀하게 따지면
    - Distance는 거리 값을 나타내는 스칼라를 말한다.
    - Metric은 미분기하학적 측면에서 텐서를 말한다.

### 노름 공간

- ![](http://latex.codecogs.com/gif.latex?V)를 체 ![](http://latex.codecogs.com/gif.latex?F)위에서 정의된 벡터 공간이라고 하자. 함수 ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Ccdot%20%5C%7C%3A%20V%5Cto%5Cmathbb%7BR%7D)가 임의의 ![](http://latex.codecogs.com/gif.latex?%5Cmathbf%7Bx%7D%2C%5Cmathbf%7By%7D%5Cin%20V)와 임의의 ![](http://latex.codecogs.com/gif.latex?c%5Cin%20F)에 대해, 다음 조건을 만족하면 노름(Norm)이라고 한다.
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D%5C%7C%5Cge%200)
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D%5C%7C%3D0%20%5CLeftrightarrow%20%5Cmathbf%7Bx%7D%3D%5Cmathbf%7B0%7D)
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%20c%5Cmathbf%7Bx%7D%5C%7C%3D%7Cc%7C%5C%7C%5Cmathbf%7Bx%7D%5C%7C)
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D&plus;%5Cmathbf%7By%7D%5C%7C%5Cle%20%5C%7C%5Cmathbf%7Bx%7D%5C%7C&plus;%5C%7C%5Cmathbf%7By%7D%5C%7C)
- 노름이 주어지는 벡터 공간을 노름 공간(Norm Space)이라고 한다.

### 내적 공간

- ![](http://latex.codecogs.com/gif.latex?V)를 체 ![](http://latex.codecogs.com/gif.latex?F%5C%3B%28F%3D%5Cmathbb%7BR%7D%5Ctext%7B%20or%20%7D%5Cmathbb%7BC%7D%29) 위에 주어진 벡터 공간이라고 하자. 함수 ![](http://latex.codecogs.com/gif.latex?%28%5Ccdot%2C%5Ccdot%29%3AV%5Ctimes%20V%5Cto%20F)가 임의의 ![](http://latex.codecogs.com/gif.latex?%5Cmathbf%7Bx%7D%2C%5Cmathbf%7By%7D%2C%5Cmathbf%7Bz%7D%5Cin%20V)와 ![](http://latex.codecogs.com/gif.latex?c%5Cin%20F)에 대해, 다음 조건을 만족하면 ![](http://latex.codecogs.com/gif.latex?%28%5Ccdot%2C%5Ccdot%29)를 내적(Inner Product)이라고 한다.
    - ![](http://latex.codecogs.com/gif.latex?%5C%7C%5Cmathbf%7Bx%7D%5C%7C%5Cge%200)
        - ![](http://latex.codecogs.com/gif.latex?%28%5Cmathbf%7Bx%7D%2C%5Cmathbf%7Bx%7D%29%3D0%20%5CLeftrightarrow%20%5Cmathbf%7Bx%7D%3D0)
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