# 5장 오차역전파법 Backpropagation

이번 장에서는 가중치 매개변수의 기울기를 효율적으로 계산하는 **오차역전파법(backpropagation)**을 배워보겠습니다. 오차역전파법을 제대로 이해하는 방법은 두 가지가 있을 것입니다. 하나는 수식을 통한 것이고, 다른 하나는 계산 그래프를 통한 것입니다. 전자 쪽이 일반적인 방법으로, 특히 기계학습을 다루는 책 대부분은 수식을 중심으로 이야기를 전개합니다. 확실히 수식을 사용한 설명은 정확하고 간결하므로 올바른 방법이라 할 수 있겠죠. 하지만 졸업 후 너무 오랜만에 수식을 중심으로 생각하다 보면 본질을 놓치거나, 수많은 수식에 당황하는 일이 벌어지기도 합니다. 그래서 이번 장에서는 계산 그래프를 사용해서 ‘시각적’으로 이해시켜드리겠습니다. 그런 다음 실제로 코드를 작성해보면 ‘과연!’이란 탄성과 함께 더 깊이 이해하게 될 것입니다.


## Copyrights
1. textbook official repository: https://github.com/WegraLee/deep-learning-from-scratch
    * 아래 python code들은 [chapter 5](https://github.com/WegraLee/deep-learning-from-scratch/tree/master/ch05)에서 가져왔습니다.
1. fork source: https://github.com/ExcelsiorCJH/DLFromScratch [(chapter5)](https://nbviewer.org/github/ExcelsiorCJH/DLFromScratch/blob/master/Chap05-BackPropagation/Chap05-Backpropagation.ipynb)
1. additional repository: https://github.com/SDRLurker/deep-learning [(5장)](https://nbviewer.org/github/SDRLurker/deep-learning/blob/master/5장.ipynb)

### Customized by Gil-Jin Jang

## 파일 설명
| 파일명 | 파일 용도 | 관련 절 | 페이지 |
|:--   |:--      |:--    |:--      |
| [Chap05-Backpropagation.ipynb](Chap05-Backpropagation.ipynb) | 내용 + 실행가능 코드 | 5.1-5.8 | 147-187 |
| [buy_apple.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/buy_apple.py) | 사과 2개를 구입하는 예제의 순전파와 역전파 구현입니다. | 5.4.1 곱셈 계층 | 162 |
| [buy_apple_orange.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/buy_apple_orange.py) | 사과와 오랜지를 구입하는 예제의 순전파와 역전파 구현입니다. | 5.4.2 덧셈 계층 | 163 |
| [gradient_check.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/gradient_check.py) | 수치 미분 방식과 비교하여 오차역전파법으로 구한 기울기를 검증합니다(기울기 확인). | 5.7.3 오차역전파법으로 구한 기울기 검증하기 | 184 |
| [layer_naive.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/layer_naive.py) | 곱셈 계층과 덧셈 계층의 구현입니다. | 5.4.1 곱셈 계층 / 5.4.2 덧셈 계층 | 161, 163 |
| [train_neuralnet.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/train_neuralnet.py) | 4장의 train_neuralnet.py와 같습니다. 단, 수치 미분 대신 오차역전파법으로 기울기를 구합니다. | 5.7.4 오차역전파법을 사용한 학습 구현하기 | 186 |
| [two_layer_net.py](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05/two_layer_net.py) | 오차역전파법을 적용한 2층 신경망 클래스 | 5.7.2 오차역전파법을 적용한 신경망 구현하기 | 181 |

위의 python code들은 [WegraLee, 5장](https://github.com/WegraLee/deep-learning-from-scratch/blob/master/ch05)에서 볼 수 있습니다. 
