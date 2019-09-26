FROM ndphu/golang-alpine:1.13

WORKDIR /opt/monitor-service

RUN git clone https://github.com/ndphu/monitor-service.git . && \
	go build

CMD /opt/monitor-service/monitor-service

