FROM pveber/bistro-base:buster

RUN apt-get update && apt-get install -y python
RUN wget http://cab.spbu.ru/files/release3.14.0/SPAdes-3.14.0.tar.gz
RUN tar -xzf SPAdes-3.14.0.tar.gz
RUN apt-get install -y cmake zlib1g-dev libbz2-dev
RUN cd SPAdes-3.14.0 && PREFIX=/usr ./spades_compile.sh
