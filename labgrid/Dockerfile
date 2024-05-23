FROM docker.io/fedora:40
# install dependencies
RUN dnf install -y python3-pip python3-setuptools python3-ansicolors \
    python3-attrs python3-autobahn python3-jinja2 python3-pexpect \
    python3-pytest python3-pyudev python3-pyusb python3-pyyaml python3-requests \
    ser2net gcc readline-devel wget patch
# install microcom
RUN wget https://github.com/pengutronix/microcom/releases/download/v2023.09.0/microcom-2023.09.0.tar.xz && \
    tar xf microcom-2023.09.0.tar.xz && cd microcom-2023.09.0 && \
    ./configure && make && make install
# install package
RUN pip install labgrid
# patch labgrid
RUN cd /usr/local/lib/python3.12/site-packages/labgrid && \
    curl https://github.com/labgrid-project/labgrid/commit/f7a1d38e89bead91cb92fb3c101353255070556b.patch | \
    patch -p 2 && \
    curl https://github.com/NickCao/labgrid/commit/fba66f5002728c1a9694616e8a68b3d30afc7864.patch | \
    patch -p 2
