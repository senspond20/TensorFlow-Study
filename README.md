# TensorFlow

+ 텐서플로우(TensorFlow) =  텐서(Tensor) + 플로우(Flow) 

+ Install TensorFlow
https://www.tensorflow.org/install/pip?hl=ko#system-install

```
# Requires the latest pip
pip install --upgrade pip

# Current stable release for CPU and GPU
pip install tensorflow

# Or try the preview build (unstable)
pip install tf-nightly
```

+ Anaconda 를 이용한 방법
https://www.anaconda.com/products/individual/download-success


+ Anaconda에 tensorflow 설치
```
conda update conda
conda install tensorflow
```

## **용어**
### **오퍼레이션(Operation)**
> 그래프 상의 노드는 오퍼레이션(줄임말 op)으로 불립니다. 오퍼레이션은 하나 이상의 텐서를 받을 수 있습니다. 오퍼레이션은 계산을 수행하고, 결과를 하나 이상의 텐서로 반환할 수 있습니다.

### **텐서(Tensor)**
>내부적으로 모든 데이터는 텐서를 통해 표현됩니다. 텐서는 일종의 다차원 배열인데, 그래프 내의 오퍼레이션 간에는 텐서만이 전달됩니다. (Caffe의 Blob과 유사합니다.)

> 벡터와 행렬을 일반화한 것이고 고차원으로 확장가능합니다. 내부적으로 텐서플로는 기본적으로 제공되는 자료형을 사용해 n-차원 배열로 나타냅니다.
- 공식홈페이지 가이드(https://www.tensorflow.org/guide/tensor?hl=ko)

### **세션(Session)**
> 그래프를 실행하기 위해서는 세션 객체가 필요합니다. 세션은 오퍼레이션의 실행 환경을 캡슐화한 것입니다.

### **변수(Variables)**
> 변수는 그래프의 실행시, 패러미터를 저장하고 갱신하는데 사용됩니다. 메모리 상에서 텐서를 저장하는 버퍼 역할을 합니다.


ref : https://davinci-ai.tistory.com/23


### **난수 생성**

+ Uniform(균일) 분포 난수
```
rand = tf.random.uniform([1], 0, 1)
```
+ Normal(정규) 분포 난수
```
rand = tf.random.normal([1],0,1)
```

### **뉴런(Neuron)**

+ 뉴런은 신경망의 가장 기본적인 구성요소입니다. 이를 퍼셉트론이라고도 부르며, 입력을 받아서 계산하여 출력하는 구조로 이루어집니다.

### **경사 하강법(Gradient Descent)**
+ 손실(error, cost)의 최소값을 찾기 위해서 그레디언트 반대 방향으로 정의한 step size를 사용하여 조금씩 변화하면서 최적의 값을 찾아가는 방식입니다