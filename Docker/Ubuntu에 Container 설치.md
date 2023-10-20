### 1. ubuntu 이미지 다운

```
// 특정 버전 다운
docker pull ubuntu:22.04

// latest 버전 다운
docker pull ubuntu:latest
docker pull ubuntu
```

### 2. 컨테이너 생성

```
docker run [옵션] [이미지] [명령어] [인자]

// 예시
docker run -it --name test ubuntu:latest bash
```

#### 옵션 종류

| option                | description                                                        |
| --------------------- | ------------------------------------------------------------------ |
| -i <br> --interactive | 컨테이너의 표준 입력(stdin)을 활성화 <br> 보통 -t 옵션과 같이 쓰임 |
| -t <br> --tty         | 가상 터미널(pseudo-TTY)을 활성화                                   |
| --name                | 컨테이너 이름 설정                                                 |
| -d <br> --detach      | 데몬 모드라고 부르며, 컨테이너를 백그라운드로 실행                 |
| --rm                  | 컨테이너가 종료될 때 자동으로 삭제                                 |
| -p <br> --publish     | 호스트와 컨테이너의 포트 연결 (포트포워딩)                         |

// TODO: 이미지, 명령어, 인자

### 3. 컨테이너 실행

```
docker start [컨테이너 ID 혹은 컨테이너 이름]

// 예시
docker start test
```

### 4. 컨테이너 접속

```
docker exec -it [컨테이너 ID 혹은 컨테이너 이름]

// 예시
docker exec -it test bash
```
