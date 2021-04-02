우분투 20.04 버전을 설치했다.

고정 ip 설정

`cd /etc/netplan`

netplan 안에 yaml 파일이 하나 있다. `sudo vi 01-network-manager-all.yaml`로 들어가자. 

yaml 파일을 들어가면 다음과 같이 초기설정 되어있다.

```yaml
network:
  version: 2
  renderer: NetworkManager
```

이 파일을 다음과 같이 수정하자.

```yaml
network:
  version: 2
  renderer: NetworkManager
  ethernets:
    eno2: # ip addr 로 네트워크 드라이브명을 확인한다.
      addresses: [ip주소/prefix] 
      # subnetmask가 255.255.255.0 일 때의 prefix : 24
      # subnetmask가 255.255.254.0 일 때의 prefix : 23
      gateway4: [gateway주소]
      nameservers: 
        addresses: [dns서버, 보조dns서버]
```

파일 수정이 끝났으면, `sudo netplan apply` 를 하고 `reboot` 를 한다.

부팅 후 컴퓨터가 다시 켜지면 네트워크가 연결된 것을 확인할 수 있다.

------

네트워크가 연결이 잘 안될 때 확인하는 방법 중 하나로 ping 을 쓸 수 있다. 

`ping 8.8.8.8` 또는 `ping 로컬ip주소` 또는 `ping 게이트웨이주소` 등등 ping 을 활용해서 확인할 수 있다.