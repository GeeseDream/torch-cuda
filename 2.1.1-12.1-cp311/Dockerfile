FROM nvidia/cuda:12.1.0-devel-ubuntu22.04

RUN apt update && apt install -y \
        build-essential \
        cmake \
        git \
        curl \
        vim \
        wget \
        ca-certificates \
        python3.11 \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*
RUN curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py && python3 get-pip.py && rm get-pip.py
RUN pip install --no-cache-dir --upgrade pip && pip install --no-cache-dir torch==2.1.1+cu121 torchvision==0.16.1+cu121 torchaudio==2.1.1+cu121 -f https://download.pytorch.org/whl/torch_stable.html