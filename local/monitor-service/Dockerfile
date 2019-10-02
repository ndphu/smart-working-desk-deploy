FROM ndphu/golang-alpine:1.13

WORKDIR /opt/monitor-service

RUN git  -c http.sslVerify=false clone https://github.com/ndphu/monitor-service.git . && \
	rm -f go.sum go.mod && \ 
	go mod init monitor-service && \
	go build

CMD /opt/monitor-service/monitor-service

