FROM python:3.12-slim
USER root 
RUN apt-get update && apt-get install -y \
    wget \
    bzip2 \
    ca-certificates \
    curl \
    git \
    gcc \
    g++ \
    build-essential \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

    RUN wget -O /tmp/miniconda.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-aarch64.sh && \
    chmod +x /tmp/miniconda.sh && \
    ls -l /tmp/miniconda.sh  # Verify that the file exists and is executable

RUN apt install build-essential
RUN bash /tmp/miniconda.sh -b -p /opt/miniconda && \
    rm /tmp/miniconda.sh
ENV PATH="/opt/miniconda/bin:$PATH"
RUN conda init bash && conda init zsh
    
RUN pip install jupyter
WORKDIR /jupyter
ADD . /jupyter/