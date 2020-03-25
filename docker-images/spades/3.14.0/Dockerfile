FROM pveber/bistro-base:buster

RUN wget http://cab.spbu.ru/files/release3.14.0/SPAdes-3.14.0-Linux.tar.gz
RUN cd usr && tar xvfz ../SPAdes-3.14.0-Linux.tar.gz --strip-components=1
RUN apt-get update && apt-get install -y python
