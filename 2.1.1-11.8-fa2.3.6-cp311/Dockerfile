FROM geesedream/torch-cuda:2.1.1-11.8-cp311

RUN apt update && apt install -y python3.11-dev
RUN git clone -b v2.3.6 https://github.com/Dao-AILab/flash-attention.git \
    && pip --no-cache-dir install packaging \
    && cd flash-attention \
    && pip --no-cache-dir install . \
    && pip --no-cache-dir install csrc/layer_norm \
    && cd.. \
    && rm -rf flash-attention
