FROM ubuntu

RUN apt-get update && \
    apt-get install -y cron

# 개발자가 넣어두고 싶은 파일들을 docker의 이미지에 복사하고 싶을 때 쓰는 명령어
# Container를 실행할 때 ch01(현재 이 도커파일의 경로)의 scripts 폴더를 복사해 넣어두어라
COPY scripts/ /scripts/
RUN chmod +x /scripts/*.sh

CMD ["cron", "-f"]