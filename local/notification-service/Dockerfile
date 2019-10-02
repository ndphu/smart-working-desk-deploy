FROM ndphu/golang-alpine:1.13

EXPOSE 8080

WORKDIR /opt/notification-service

RUN git -c http.sslVerify=false clone https://github.com/ndphu/notification-service.git . && \
	rm -f go.sum go.mod && \ 
	go mod init notification-service && \
	go build

CMD /opt/notification-service/notification-service


