FROM ubuntu:18.04

RUN apt-get update && apt-get install -y curl
WORKDIR /app
RUN curl https://gist.githubusercontent.com/matti/ac4dd1c49225c693880457a604f615ab/raw/8198b6993124c681a77838a93fcd7c9bf731c1c6/skaffolder.sh > skaffolder.sh
RUN chmod +x skaffolder.sh

COPY app .

CMD ["./entrypoint.sh"]
ENTRYPOINT [ "/app/skaffolder.sh" ]
