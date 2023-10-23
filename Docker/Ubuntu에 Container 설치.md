### 1. ubuntu 이미지 다운

```
// 특정 버전 다운
docker pull ubuntu:22.04

// latest 버전 다운
docker pull ubuntu:latest
docker pull ubuntu
```

---

### 2. 컨테이너 생성

```
docker run [옵션] [이미지] [명령어] [인자]

// 예시
docker run -it --name test ubuntu:latest bash
```

| 위 cli를 입력 시 컨테이너로 접속되는데, exit로 컨테이너를 나오면 자동으로 실행이 중지되기 때문에 이후에 실행 작업을 거친다.

#### 옵션 종류

| option                | description                                                        |
| --------------------- | ------------------------------------------------------------------ |
| -i <br> --interactive | 컨테이너의 표준 입력(stdin)을 활성화 <br> 보통 -t 옵션과 같이 쓰임 |
| -t <br> --tty         | 가상 터미널(pseudo-TTY)을 활성화                                   |
| --name                | 컨테이너 이름 설정                                                 |
| -d <br> --detach      | 데몬 모드라고 부르며, 컨테이너를 백그라운드로 실행                 |
| --rm                  | 컨테이너가 종료될 때 자동으로 삭제                                 |
| -p <br> --publish     | 호스트와 컨테이너의 포트 연결 (포트포워딩)                         |

#### 이미지란?

소스 코드, 라이브러리, 종속성, 도구 및 응용 프로그램을 실행하는데 필요한 기타 파일을 포함하는 불변 파일이다.

```
// 이미지 이름 양식
[저장소 이름]/[이미지 이름]:[태그]

// 예시
mdock/my-app:tagname
```

---

### 3. 컨테이너 실행

```
docker start [컨테이너 ID 혹은 컨테이너 이름]

// 예시
docker start test
```

---

### 4. 컨테이너 접속

```
docker exec -it [컨테이너 ID 혹은 컨테이너 이름]

// 예시
docker exec -it test bash
```

---
