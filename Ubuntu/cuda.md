## Ubuntu20.04에 Cuda 설치하기

```
sudo apt update
sudo apt install cuda
nvidia-smi

cd Downloads
tar xvf cudnn-11.2-linux-x64-v8.1.1.33.solitairetheme8

cd cuda

sudo cp include/cudnn* /usr/local/cuda-11.2/include
sudo cp lib64/libcudnn* /usr/local/cuda-11.2/lib64/
sudo chmod a+r /usr/local/cuda-11.2/lib64/libcudnn*
```

### cuda가 잘 깔렸는지 확인하기

```
cat /usr/local/cuda-11.2/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
```

