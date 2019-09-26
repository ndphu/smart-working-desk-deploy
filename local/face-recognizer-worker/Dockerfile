FROM ndphu/ubuntu-goface:latest

WORKDIR /opt/face-recognizer-worker

RUN git clone https://github.com/ndphu/face-recognizer-worker.git . && \
	go mod edit -replace github.com/Kagami/go-face=/go/src/github.com/Kagami/go-face && \
	go build

CMD /opt/face-recognizer-worker/face-recognizer-worker




