## CUDA 환경변수 설정

```
export PATH=/usr/local/cuda-11.1/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-11.1/lib64:$LD_LIBRARY_PATH
export CUDA_HOME='/usr/local/cuda-11.1'
```

## NVIDIA driver 설치 확인
`cat /proc/driver/nvidia/version`
`nvidia-smi`

## cuda 확인
`nvcc --version`

## cudnn 확인
`cat /usr/local/cuda/include/cudnn_version.h | grep CUDNN_MAJOR -A 2`
