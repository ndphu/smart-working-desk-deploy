FROM ndphu/ubuntu-go:1.13

RUN apt-get update && \
	apt-get install -y  wget unzip git cmake build-essential libjpeg-dev libblas-dev pkg-config libatlas-base-dev && \
	wget -O dlib.zip https://codeload.github.com/davisking/dlib/zip/v19.17  && \
	unzip dlib.zip && \
	mv dlib-19.17 dlib && \
	mkdir -p /dlib/build && \
	cd /dlib/build && cmake .. && \
	make -j 4 && \
	make install && \
	ldconfig && \
	sed -i 's/^Libs: .*/& -lblas -llapack/' /usr/local/lib/pkgconfig/dlib-1.pc && \
	rm -rf /dlib*

