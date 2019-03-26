FROM pkdogcom/pytorch:0.4.1-py3
LABEL maintainer pkdogcom@gmail.com

# Install visualization tools and the libraries for pycharm
RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y protobuf-compiler gedit libgtk2.0-0 libcanberra-gtk-module libxext-dev libxrender-dev libxtst-dev git subversion \
        mercurial && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/* && \
    pip install -U torchvision numpy && \
    # Use Pillow-SIMD for faster preprocessing using PIL API
    pip uninstall -y pillow && pip install pillow-simd && \
    pip install tensorflow html5lib==0.999999999 # In order to use Tensorboard

WORKDIR /root

