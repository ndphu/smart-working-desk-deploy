FROM ndphu/golang-alpine:1.13

EXPOSE 8080

WORKDIR /opt/face-service

RUN git -c http.sslVerify=false clone https://github.com/ndphu/face-service.git . && \
	rm -f go.sum go.mod && \ 
	go mod init face-service && \
	go build

CMD /opt/face-service/face-service

