# Jupyter Notebook kernle 추가 및 삭제

### 가상환경 생성

`conda create -n py36 python=3.6`

### 가상환경 활성화

`conda activate py36`

### ipykernel 패키지 설치

`pip install ipykernel`

### 커널 추가

`python -m ipykernel install --user --name 가상환경이름`  

`python -m`은 현재 활성화 된 가상환경의 python 모듈을 사용한다는 것이다. 

### 커널 제거

`jupyter kernelspec uninstall 가상환경이름`
