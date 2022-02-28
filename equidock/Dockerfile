FROM nvidia/cuda:11.1-cudnn8-runtime-ubuntu18.04

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
      python3-pip \
      && rm -rf /var/lib/apt/lists/*
RUN pip3 install --upgrade pip
COPY requirements.txt .
RUN pip install -r requirements.txt 
COPY . .
ENTRYPOINT ["python3", "inference_rigid.py"]
