FROM docker.io/fedora:40
# install dependencies
RUN dnf install -y python3-pip python3-devel git patch gcc jq moreutils
# clone repository
RUN git clone https://github.com/NickCao/crossbar
# install package
RUN pip install ./crossbar
