 
# 기반 이미지 선택 
FROM ubuntu:22.04

# 사용 포트 명시
EXPOSE 8080

# 환경 변수 설정
ENV APP_NAME MyDockerApp

# 컨테이너 안에서 작업될 디렉터리 지정
WORKDIR /app

# 로컬 파일을 컨테이너 내부로 복사하겠다
# 로컬 파일 : 도커 파일이 있는 디렉터리의 모든 파일
COPY hello.py .

# 필요한 라이브러리 설치 

RUN apt update
RUN apt install -y python3
# RUN apt update && apt install -y python3

# cmd에 python3를 쓸 필요가 없다.
# 고정 실행 명령어가 된다.
ENTRYPOINT ["python3"]

# 컨테이너가 실행될 때 실행할 명령이다. 
# CMD ["python3", "hello.py"]
CMD ["hello.py"]