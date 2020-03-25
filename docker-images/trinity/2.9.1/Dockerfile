FROM pveber/bistro-base:buster

RUN apt-get update && \
    apt-get install -y --allow-unauthenticated libc6 libgcc1 libgomp1 libhts2 libstdc++6 perl jaligner \
    libcommons-collections4-java libgetopt-java libjung-free-java bowtie bowtie2 \
    python libwww-perl default-jre-headless samtools jellyfish r-base-core \
    r-cran-cluster r-bioc-qvalue rsem berkeley-express trimmomatic \
    transdecoder parafly curl salmon cmake
RUN wget "https://github.com/trinityrnaseq/trinityrnaseq/releases/download/v2.9.1/trinityrnaseq-v2.9.1.FULL.tar.gz"
RUN tar xvfz trinityrnaseq-v2.9.1.FULL.tar.gz
RUN cd trinityrnaseq-v2.9.1 && make && make plugins
RUN cd trinityrnaseq-v2.9.1 && ln -s $PWD/Trinity /usr/bin
RUN apt-get install -y python-numpy
ENV TRINITY_HOME /trinityrnaseq-Trinity-v2.9.1
