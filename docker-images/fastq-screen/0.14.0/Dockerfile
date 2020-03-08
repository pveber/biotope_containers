FROM pveber/bistro-base:buster

RUN apt-get update && apt-get -y install bowtie2

RUN perl -MCPAN -e "install GD"

RUN wget https://www.bioinformatics.babraham.ac.uk/projects/fastq_screen/fastq_screen_v0.14.0.tar.gz && \
    tar xzf fastq_screen_v0.14.0.tar.gz && \
    rm fastq_screen_v0.14.0.tar.gz && \
    ln -s /fastq_screen_v0.14.0/fastq_screen /usr/bin/fastq_screen
