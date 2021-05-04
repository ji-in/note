### ImportError: No module named PIL.Image

```
pip install pillow
```

### VNML: Driver/library version mismatch

`$ lsmod | grep nvidia`

`$ sudo rmmod nvidia_drm`

`$ sudo rmmod nvidia_modeset`

`$ sudo rmmod nvidia_uvm`

`$ sudo rmmod nvidia`

만약 `rmmod:ERROR: Module nvidia is in use`와 같은 에러가 난다면, `$ sudo lsof /dev/nvidia*`를 사용하여 현재 nvidia 관련 프로세스를 확인한 뒤에 `sudo kill -9 PID`를 사용하여 프로세스를 강제 종료시켜주면 된다.

마지막으로 `$ nvidia-smi`를 사용하면 정상적인 결과를 볼 수 있다.

