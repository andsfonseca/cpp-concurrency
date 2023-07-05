FROM mambaorg/micromamba:focal

COPY --chown=$MAMBA_USER:$MAMBA_USER env.yaml /tmp/env.yaml

RUN micromamba install -y -n base -f /tmp/env.yaml && \
    micromamba clean --all --yes

ARG MAMBA_DOCKERFILE_ACTIVATE=1  

USER root

RUN apt-get update && \
    apt-get -y install build-essential 
