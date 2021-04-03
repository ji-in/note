### Nvidia driver 삭제하기

`*sudo apt-get remove --purge '^nvidia-.\*'*`

### CUDA 삭제하기

`*sudo apt-get --purge remove 'cuda\*'`

`*sudo apt-get autoremove --purge 'cuda\*'*'`

### CUDA 파일 삭제하기

`*sudo rm -rf /usr/local/cuda*`