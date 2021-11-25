# 6장 학습 관련 기술들
이번 장에서는 신경망 학습의 핵심 개념들을 만나봅니다. 이번 장에서 다룰 주제는 가중치 매개변수의 최적값을 탐색하는 최적화 방법, 가중치 매개변수 초깃값, 하이퍼파라미터 설정 방법 등, 모두가 신경망 학습에서 중요한 주제입니다. 오버피팅의 대응책인 가중치 감소와 드롭아웃 등의 정규화 방법도 간략히 설명하고 구현해봅니다. 마지막으로 최근 많은 연구에서 사용하는 배치 정규화도 짧게 알아봅니다. 이번 장에서 설명하는 기법을 이용하면 신경망(딥러닝) 학습의 효율과 정확도를 높일 수 있습니다. 


## Copyrights
1. textbook official repository: https://github.com/WegraLee/deep-learning-from-scratch
1. fork source: https://github.com/ExcelsiorCJH/DLFromScratch 
    - [[밑러닝]_Chap06-학습관련기술들.pdf](https://github.com/ExcelsiorCJH/DLFromScratch/blob/master/Chap06-Training_Models/%5B%EB%B0%91%EB%9F%AC%EB%8B%9D%5D_Chap06-%ED%95%99%EC%8A%B5%EA%B4%80%EB%A0%A8%EA%B8%B0%EC%88%A0%EB%93%A4.pdf)
1. additional repository: https://github.com/SDRLurker/deep-learning 
    - 아래 대부분의 내용은 [(6장)](https://nbviewer.org/github/SDRLurker/deep-learning/blob/master/6장.ipynb) 에서 가져왔습니다.

### Customized by Gil-Jin Jang


## 파일 설명
| 파일명 | 파일 용도 | 관련 절 | 페이지 |
|:--   |:--      |:--    |:--      |
| [Chap06-Training.ipynb](Chap06-Training.ipynb) | 내용 + 실행가능 코드 | 6.1-6.6 | 189-226 |
| [Chap06-AdaDelta.ipynb](Chap06-AdaDelta.ipynb) | Adam의 학습 패턴 | 6.1.6 Adam | 199 |
| [batch_norm_gradient_check.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/batch_norm_gradient_check.py) | 배치 정규화를 구현한 신경망의 오차역전파법 방식의 기울기 계산이 정확한지 확인합니다(기울기 확인). |  |  |
| [batch_norm_test.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/batch_norm_test.py) | MNIST 데이터셋 학습에 배치 정규화를 적용해봅니다. | 6.3.2 배치 정규화의 효과 | 212 |
| [hyperparameter_optimization.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/hyperparameter_optimization.py) | 무작위로 추출한 값부터 시작하여 두 하이퍼파라미터(가중치 감소 계수, 학습률)를 최적화해봅니다. | 6.5.3 하이퍼파라미터 최적화 구현하기 | 224 |
| [optimizer_compare_mnist.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/optimizer_compare_mnist.py) | SGD, 모멘텀, AdaGrad, Adam의 학습 속도를 비교합니다. | 6.1.8 MNIST 데이터셋으로 본 갱신 방법 비교 | 201 |
| [optimizer_compare_naive.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/optimizer_compare_naive.py) | SGD, 모멘텀, AdaGrad, Adam의 학습 패턴을 비교합니다. | 6.1.7 어느 갱신 방법을 이용할 것인가? | 200 |
| [overfit_dropout.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/overfit_dropout.py) | 일부러 오버피팅을 일으킨 후 드롭아웃(dropout)의 효과를 관찰합니다. | 6.4.3 드롭아웃 | 219 |
| [overfit_weight_decay.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/overfit_weight_decay.py) | 일부러 오버피팅을 일으킨 후 가중치 감소(weight_decay)의 효과를 관찰합니다. | 6.4.1 오버피팅 | 215 |
| [weight_init_activation_histogram.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/weight_init_activation_histogram.py) | 활성화 함수로 시그모이드 함수를 사용하는 5층 신경망에 무작위로 생성한 입력 데이터를 흘리며 각 층의 활성화값 분포를 히스토그램으로 그려봅니다. | 6.2.2 은닉층의 활성화값 분포 | 203 |
| [weight_init_compare.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06/weight_init_compare.py) | 가중치 초깃값(std=0.01, He, Xavier)에 따른 학습 속도를 비교합니다. | 6.2.4 MNIST 데이터셋으로 본 가중치 초깃값 비교 | 209 |

위의 python code들은 [WegraLee, 6장](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch06)에서 볼 수 있습니다. 
