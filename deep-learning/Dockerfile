FROM pkdogcom/pytorch:0.4.1-py3
LABEL maintainer pkdogcom@gmail.com

# Install Caffe
RUN apt-get update && apt-get install -y caffe-cuda  # The transitive dependency on python3-tk will hang and thus we have to manually run the script in a container instead

# Install Tensorflow
RUN apt-get update && apt-get upgrade -y && \
    pip3 install tensorflow-gpu==1.10.0 html5lib==0.9999999 && \
    # Use Pillow-SIMD for faster preprocessing using PIL API
    pip3 uninstall -y pillow && pip3 install pillow-simd
