## Ubuntu20.04에 아나콘다 설치하는 방법

```
$ wget  [아나콘다 설치 링크]
$ bash Anaconda3-2020.11-Linux-x86_64.sh
```

`Enter`를 누르면 라이센스를 확인하는 창이 나온다. 확인창이 너무 길다. `Ctrl+c`를 누르자.

[yes|no]로 질문을 계속 하면, yes를 입력하자. 무조건 yes다.

conda 명령어를 사용하기 위해서는 아래의 명령어를 쳐야 한다.

```
$ sudo vi ~/.bashrc
```

텍스트 편집기가 열리면 마지막 줄에 다음 코드를 추가하고 저장한다.

```
export PATH=~/anaconda3/bin:~/anaconda3/condabin:$PATH
```

이후 터미널에서 다음 명령어를 입력하면 아나콘다 프롬프트가 열리고 앞에 (bash)가 붙게 된다.

```
$ source ~/.bashrc
```

`conda -V`를 사용해 conda가 잘 설치됐는지 확인한다.



터미널을 실행할 때마다 아마콘다 프롬프트로 설정이 되어있다. 아나콘다 프롬프트를 없애기 위해 다음 명령어를 입력하고 터미널을 새로 시작하면 (base)가 없어진 것을 확인할 수 있다.

```
$ conda config --set auto_activate_base False
```



아나콘다 프롬프트를 다시 실행하려면 `conda activate`

아나콘다 프롬프트를 끄려면 `conda deactivate`

[참고한 블로그](https://ieworld.tistory.com/12)