# Docker Run
1. tutorial container 실행
    ```bash
    docker run -d -p 80:80 docker/getting-started
    ```
    - `-d`: 분리 모드(백그라운드)에서 컨테이너 실행  
    - `-p 80:80`: 호스트의 포트 80을 컨테이너의 포트 80에 매핑  
    - `docker/getting-started`: 사용할 이미지  
    - Tip  
        - 단일 문자 플래그를 결합하여 전체 명령을 단축할 수 있다.  
        - 위 명령을 아래와 같이 사용가능  
        ```bash
        docker run -dp 80:80 docker/getting-started
        ```