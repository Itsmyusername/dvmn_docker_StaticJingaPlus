ARG version=22.04
FROM ubuntu:${version}

ENV DEBIAN_FRONTEND=noninteractive

ARG staticjinja_plus_branch=main

RUN apt-get update -y \
    && apt-get install -y python3 python3-venv \
    && rm -rf /var/lib/apt/lists/*

ADD --checksum=sha256:${hash_sum} https://github.com/MrDave/StaticJinjaPlus/archive/refs/tags/${staticjinja_plus_version}.tar.gz staticjinja.tar.gz
RUN tar -xzf staticjinja.tar.gz && \
    rm staticjinja.tar.gz
        
        
WORKDIR /StaticJinjaPlus-${staticjinja_plus_version}

RUN python3 -m venv .venv && \
    . .venv/bin/activate && \
    .venv/bin/pip install --no-cache-dir -r requirements.txt

CMD [".venv/bin/python", "main.py"]