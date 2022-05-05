# 도커 설치
## 도커 설치 (VM과 SSH로 연결한 콘솔에서 실행)

- [apt(Advance Packging Tools)](https://tttap.tistory.com/130) linux packages update
- update - 설치 가능한 패키지 리스트를 최신화
- upgrade - 실제 업데이트

`sudo apt update`

- `--yes`는 `-y`로 약어로 표현 가능 [[-y Flag의 의미](https://webisfree.com/2018-10-08/[linux]-apt-get-install-%EC%9D%B8%EC%8A%A4%ED%86%A8%EC%97%90%EC%84%9C-y-flag%EC%9D%98-%EC%9D%98%EB%AF%B8)]

`sudo apt install --yes apt-transport-https ca-certificates curl gnupg2 software-properties-common`

- 위 내용은 아래와 같은 결과 [[도커 다운을 위해 필요한 패키지 설치](https://roseline124.github.io/kuberdocker/2019/07/17/docker-study02.html)]

    >sudo apt install --yes apt-transport-https  
    >sudo apt install --yes ca-certificates  
    >sudo apt install --yes curl  
    >sudo apt install --yes gnupg2  
    >sudo apt install --yes software-properties-common  

- curl 명령어로 도커 다운받기

`curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -`

- repository에 경로 추가하기

`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"`

`sudo apt update`

- 도커 설치하기

`sudo apt install --yes docker-ce`

- 참고 : [도커 개발환경 세팅 및 배포 실습](https://roseline124.github.io/kuberdocker/2019/07/17/docker-study02.html)

<br>

- sudo 명령어 없이 도커 사용을 위하여 사용자를 도커 그룹에 추가

`sudo usermod -aG docker $USER`
