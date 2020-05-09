FROM nvcr.io/nvidia/l4t-base:r32.4.2

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get -y update && \
    apt-get -y install python3 python3-pip

RUN apt-get -y update && \
    apt-get -y install python3-numpy python3-scipy python3-pandas

RUN pip3 install jupyterlab

RUN useradd -m -s /bin/bash -N -u 1000 docker
USER docker

CMD [ "jupyter", "lab", "--port=8000", "--ip=*", "--notebook-dir=/data", "--no-browser", "--NotebookApp.base_url=/jupyter"]