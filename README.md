## Docker Compose 사용법

컨테이너를 올리기 전에 Docker Desktop이 켜있는 지 확인하다.</br>
꺼져있다면 Docker Desktop이 완전히 켜지고 나서 명령어를 사용해야 한다.

### 컨테이너 시작하기
docker-compose up -d 

### 컨테이너 종료하기 (사용이 끝나면)
docker-compose down

## Bind-Mount
현재 프로젝트의 workspace 폴더는 컨테이너 안의 /opt/workspace와 바인드 마운트 되어있다.</br>
따라서, 컨테이너 내부에서 파일을 수정하거나 로컬에서 파일을 수정하면 서로 간에 영향을 주기 때문에 유의하며 사용해야 한다.

## Jupyter Lab
주피터 랩은 localhost:8888 으로 접속이 가능하다.
스파크 job을 제출 후 보는 스파크의 애플리케이션 UI는 localhost:4040 으로 접속 가능하다.

## Spark Standalone
스파크 Standalone(독립실행형 모드)로 사용 가능하다.</br>
마스터 노드의 UI는 localhost:8080, 워커 1 노드의 UI는 localhost:8081, 워커 2 노드의 UI는 localhost:8082 로 접속 가능하다.</br>

하지만, 연습에서는 환경에서는 local[*] 모드로 SparkContext(또는 SparkSession)을 사용해도 무방하기 때문에 로컬 모드로 사용하였다.
