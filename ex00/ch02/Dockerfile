# 이미지 사용 설정
FROM ubuntu

# 패키지 설치
RUN apt-get update && \
    apt-get install -y nano && \
    apt-get install locales

# 한글 입력이 가능하게 설정
RUN locale-gen ko_KR.UTF-8
    ENV LANG ko_KR.UTF-8
    ENV LC_ALL ko_KR.UTF-8

# 기본 작업 경로 설정
WORKDIR /app

# 로컬의 이미지 파일을 컨테이너로 복사
COPY ./images/image.jpg ./image.jpg

# 컨테이너 시작 시 bash 실행되게 하기
CMD ["/bin/bash"]

#컨테이너 시작 시 항상 실행되게 하기
ENTRYPOINT ["echo", "컨테이너가 실행됩니다."]