# 4장 신경망 학습 Neural Network Training

이번 장에서는 신경망 학습(training)에 대해 알아보자. **학습**이란 학습 데이터로부터 가중치 매개변수의 최적값을 자동으로 찾는것을 말한다. 또한, 이번 장에서는 신경망이 학습할 수 있도록 하는 **지표**에 해당하는 ***손실함수*** 에 대해 알아보자.

## Copyrights
1. textbook official repository: https://github.com/WegraLee/deep-learning-from-scratch
    * 아래 python code들은 [chapter 4](https://github.com/WegraLee/deep-learning-from-scratch/tree/master/ch04)에서 가져왔습니다.
1. fork source: https://github.com/ExcelsiorCJH/DLFromScratch [(chapter4)](https://nbviewer.org/github/ExcelsiorCJH/DLFromScratch/blob/master/Chap04-Neural_Network_Traing/Chap04-Neural_Network_Training.ipynb)
1. additional repository: https://github.com/SDRLurker/deep-learning [(4장)](https://nbviewer.org/github/SDRLurker/deep-learning/blob/master/4장.ipynb)


### Customized by Gil-Jin Jang


## 파일 설명

| 파일명 | 파일 용도 | 관련 절 | 페이지 |
|:--   |:--      |:--    |:--      |
| [Chap04-NN_Training.ipynb](Chap04-NN_Training.ipynb) | 내용 + 실행가능 코드 | 4.1-4.6 | 107-146 |
| [gradient_1d.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/gradient_1d.py) | 수치 미분으로 기울기를 구합니다. | 4.3.2 수치 미분의 예 | 125 |
| [gradient_2d.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/gradient_2d.py) | 수치 미분으로 기울기를 구합니다(두 편미분을 동시에 계산). | 4.4 기울기 | 129 |
| [gradient_method.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/gradient_method.py) | 경사하강법의 갱신 과정을 보여줍니다. | 4.4.1 경사법(경사 하강법) | 132 |
| [gradient_simplenet.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/gradient_simplenet.py) | simpleNet 클래스 | 4.4.2 신경망에서의 기울기 | 134 |
| [train_neuralnet.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/train_neuralnet.py) | 미치배치 방식으로 학습하고 시험 데이터로 평가합니다. | 4.5.2 미니배치 학습 구현하기 / 4.5.3 시험 데이터로 평가하기 | 141, 143 |
| [two_layer_net.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch04/two_layer_net.py) | 2층 신경망 클래스 | 4.5.1 2층 신경망 클래스 구현하기 | 137 |
