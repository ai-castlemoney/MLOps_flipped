1. virtualenv 환경설정
    - vm instance에서 진행

    ```
    # virtualenv 설치
    sudo apt install virtualenv -y

    # 가상환경 만들기 -> env 폴더가 생성됨
    virtualenv -p python3 env

    # 가상환경 활성화
    source env/bin/activate
    ````

가상환경이 제대로 활성화가 되었다면 아래와 같이 명령줄 앞에(env)라고 표기되어야 한다.
