FROM pkdogcom/opencv:3.2-cudnn6
LABEL maintainer pkdogcom@gmail.com

RUN apt-get update && apt-get install -y --no-install-recommends \
	git python-pip python-dev python-tk python-setuptools && \
    pip install --upgrade pip && \
    pip install http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp27-cp27mu-linux_x86_64.whl && \
    pip install -U torchvision numpy
    
