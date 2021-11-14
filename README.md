# DL From Scratch

### 수정사항

`equations_and_figures/` 폴더 전체와 
`dataset/`에 있는 데이터 파일들을 삭제하였습니다. 
본 repository 의 전체 크기를 줄이기 위함입니다. 
fork source인 https://github.com/ExcelsiorCJH/DLFromScratch 에는 유지되어 있습니다.

1. 아래 folder는 삭제하였습니다. 필요한 그림들은 개별 chapter에 복사되어 있습니다.
    - `equations_and_figures/`
1. 아래 python script는 유지하였습니다.
    - `dataset/mnist.py`    
1. 아래 파일들은 http://yann.lecun.com/exdb/mnist/ 에서 받을 수 있고, `dataset/mnist.py`을 실행시키면 자동으로 받을 수 있습니다.
    - `dataset/t10k-images-idx3-ubyte.gz`
    - `dataset/t10k-labels-idx1-ubyte.gz`
    - `dataset/train-images-idx3-ubyte.gz`
    - `dataset/train-labels-idx1-ubyte.gz`
1. 아래 파일은 `dataset/mnist.py`을 실행하면 자동으로 생성됩니다.
    - `dataset/mnist.pkl`


## 1. 교재 

### 밑바닥부터 시작하는 딥러닝

![](./cover.png)

## 2. 목차

아래의 목차를 클릭하면 nbviewer.jupyter.org 에서 Notebook이 열림

- 1장 - *생략*
- [2장 - 퍼셉트론](http://nbviewer.jupyter.org/github/ExcelsiorCJH/DLFromScratch/blob/master/Chap02-Perceptron/Chap02-Perceptron.ipynb)
- [3장 - 신경망](http://nbviewer.jupyter.org/github/ExcelsiorCJH/DLFromScratch/blob/master/Chap03-NeuralNetwork/Chap03-NeuralNetwork.ipynb)
- [4장 - 신경망 학습](https://github.com/ExcelsiorCJH/DLFromScratch/blob/master/Chap04-Neural_Network_Traing/Chap04-Neural_Network_Training.ipynb)
- [5장 - 오차역전파법](https://github.com/ExcelsiorCJH/DLFromScratch/blob/master/Chap05-BackPropagation/Chap05-Backpropagation.ipynb)

## 3. 참고자료

- GitHub: https://github.com/WegraLee/deep-learning-from-scratch
