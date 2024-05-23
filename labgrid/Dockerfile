FROM docker.io/fedora:40
# install dependencies
RUN dnf install -y python3-pip python3-setuptools python3-ansicolors \
    python3-attrs python3-autobahn python3-jinja2 python3-pexpect \
    python3-pytest python3-pyudev python3-pyusb python3-pyyaml python3-requests
# install package
RUN pip install labgrid
