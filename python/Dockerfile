FROM ubuntu
ENV PATH /usr/local/bin:$PATH
RUN set -eux; \
        apt-get update; \
        apt-get install -y --no-install-recommends python3.10 python3-distutils; \
        rm -rf /var/lib/apt/lists/*

# install pip
# https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py

COPY get-pip.py /etc/
RUN python3 /etc/get-pip.py

CMD ["python3"]


