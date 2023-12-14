FROM geesedream/torch-cuda:2.1.1-11.8-cp311

RUN git clone -b v2.3.6 https://github.com/Dao-AILab/flash-attention.git

RUN pip install packaging \
    && cd flash-attention \
    && MAX_JOBS=4 pip install . --no-build-isolation \
    && pip install csrc/layer_norm \
    && cd.. \
    && rm -rf flash-attention
