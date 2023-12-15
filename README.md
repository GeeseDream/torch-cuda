# Torch-CUDA Docker Images

This repository offers Docker images designed for machine learning and deep learning, built with PyTorch, CUDA, and optionally Flash-Attention. Based on the `nvidia/cuda` `ubuntu-22.04` images, they provide a streamlined setup for projects needing specific PyTorch and CUDA versions.

### Usage

Once you have pulled the required image, you can start a container using that image with the following command:

```bash
docker run -it --gpus all -v ${pwd}:/workspace -w /workspace geesedream/torch-cuda:2.1.1-cu11.8-fa2.3.6-cp311 /bin/bash
```

## Available Tags

Each image tag in the repository follows the naming convention: `torch_version-cuda_version[-fa_flash_attn_version]-cp_python_version`. If the Flash-Attention version is not specified, it means the image does not include Flash-Attention.

### Pulling Images 

To pull an image from this repository, use:

```bash
docker pull geesedream/torch-cuda:<tag>
```

### Current Tags

- [`geesedream/torch-cuda:2.1.1-cu11.8-fa2.3.6-cp311`](https://github.com/GeeseDream/torch-cuda/blob/main/2.1.1-cu11.8-fa2.3.6-cp311/Dockerfile)
  - PyTorch: 2.1.1
  - CUDA: 11.8
  - Flash-Attention: 2.3.6
  - Python: 3.11

- [`geesedream/torch-cuda:2.1.1-cu11.8-cp310`](https://github.com/GeeseDream/torch-cuda/blob/main/2.1.1-cu11.8-cp310/Dockerfile)
  - PyTorch: 2.1.1
  - CUDA: 11.8
  - Python: 3.10

- [`geesedream/torch-cuda:2.1.1-cu11.8-cp311`](https://github.com/GeeseDream/torch-cuda/blob/main/2.1.1-cu11.8-cp311/Dockerfile)
  - PyTorch: 2.1.1
  - CUDA: 11.8
  - Python: 3.11

- [`geesedream/torch-cuda:2.1.1-cu12.1-cp311`](https://github.com/GeeseDream/torch-cuda/blob/main/2.1.1-cu12.1-cp311/Dockerfile)
  - PyTorch: 2.1.1
  - CUDA: 12.1
  - Python: 3.11


## Building Images

To build an image from this repository, use:

```bash
docker build -t geesedream/torch-cuda:$TAG -f Dockerfile .
```

## END

That's it
