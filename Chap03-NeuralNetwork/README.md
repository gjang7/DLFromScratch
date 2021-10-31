# 3장 신경망 Neural Network

## Copyrights
1. textbook official repository: https://github.com/WegraLee/deep-learning-from-scratch
    * 아래 python code들은 [chapter 3](https://github.com/WegraLee/deep-learning-from-scratch/tree/master/ch03)에서 가져왔습니다.
1. fork source: https://github.com/ExcelsiorCJH/DLFromScratch [(chapter3)](https://nbviewer.org/github/ExcelsiorCJH/DLFromScratch/blob/master/Chap03-NeuralNetwork/Chap03-NeuralNetwork.ipynb)
1. additional repository: https://github.com/SDRLurker/deep-learning [(3장)](https://nbviewer.org/github/SDRLurker/deep-learning/blob/master/3%EC%9E%A5.ipynb)
1. [plot_mnist_filters.ipynb](plot_mnist_filters.ipynb)는 
[Scikit-learn MNIST 예제](https://scikit-learn.org/stable/auto_examples/neural_networks/plot_mnist_filters.html)의 
내용으로 작성되었습니다.


### Customized by Gil-Jin Jang


## 파일 설명

| 파일명 | 파일 용도 | 관련 절 | 페이지 |
|:--   |:--      |:--    |:--      |
| [Chap03-NeuralNetwork.ipynb](Chap03-NeuralNetwork.ipynb) | 내용 + 실행가능 코드 | 3.1-3.7 | 
| [plot_mnist_filters.ipynb](plot_mnist_filters.ipynb) | MNIST Neural Network 학습 및 필터 시각화 예제 | APPENDIX | 
| [mnist_show.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/mnist_show.py) | MNIST 데이터셋을 읽어와 훈련 데이터 중 0번째 이미지를 화면에 출력합니다. | 3.6.1 손글씨 데이터셋 | 99 |
| [neuralnet_mnist.py](neuralnet_mnist.py) | 신경망으로 손글씨 숫자 그림을 추론합니다. 입력층, 은닉층1, 은닉층2, 출력층의 뉴런 수는 각각 784, 50, 100, 10입니다. | 3.6.2 신경망의 추론 처리 | 100 |
| [neuralnet_mnist_batch.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/mnist_show.py) | neuralnet_mnist.py에 배치 처리 기능을 더했습니다. | 3.6.3 배치 처리 | 104 |
| [relu.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/relu.py) | ReLU 함수를 구현한 코드입니다. | 3.2.7 ReLU 함수 | 76 |
| [sample_weight.pkl](sample_weight.pkl) | 미리 학습해둔 가종치 매개변수의 값들입니다. | 3.6.2 신경망의 추론 처리 | 100 |
| [sig_step_compare.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/sig_step_compare.py) | 시그모이드 함수와 계단 함수의 그래프 모양을 비교해봅니다. | 3.2.5 시그모이드 함수와 계단 함수 비교 | 74 |
| [sigmoid.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/sigmoid.py) | 시그모이드 함수를 구현한 코드입니다. | 3.2.4 시그모이드 함수 구현하기 | 72 |
| [step_function.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch03/step_function.py) | 계단 함수를 구현한 코드입니다. | 3.2.3 계단 함수의 그래프 | 70 |
