FROM jupyter/tensorflow-notebook:2023-04-10

USER root

RUN apt-get update --yes && \
    apt-get install --yes --no-install-recommends \
    curl && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}
