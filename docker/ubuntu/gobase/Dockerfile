FROM ubuntu:18.04
RUN apt-get update && apt-get install -y  wget

RUN wget https://dl.google.com/go/go1.13.linux-amd64.tar.gz && \
	tar -xvf go1.13.linux-amd64.tar.gz && \
	mv go /usr/local && \
	rm -f /go1.13.linux-amd64.tar.gz

ENV GOROOT /usr/local/go 
ENV GOPATH $HOME/go 
ENV PATH $GOPATH/bin:$GOROOT/bin:$PATH

ADD KMS-IWSVA.cer /etc/ssl/certs/
RUN update-ca-certificates

RUN echo "insecure" >> $HOME/.curlrc


