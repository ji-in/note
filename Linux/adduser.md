## 우분투에서 user 추가하기

1. usesr 추가하기 (user 이름은 jiin)

   ```
   sudo adduser jiin
   ```

   생성할 유저를 위한 그룹과 홈 디렉토리가 생성된다.개인정보 입력하라고 나오는데, 하기 싫으면 엔터 누르기

2. sudo 그룹 추가하기

   ```
   sudo usermod -aG sudo jiin
   ```

3. 해당 user 삭제하기

   ```
   sudo deluser jiin
   ```

------

[참고한 블로그](https://psychoria.tistory.com/707)

