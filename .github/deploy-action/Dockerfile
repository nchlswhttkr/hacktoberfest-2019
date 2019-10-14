FROM ubuntu:latest

RUN apt-get update -qqy && apt-get install -qqy git

ADD entrypoint.sh /
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
