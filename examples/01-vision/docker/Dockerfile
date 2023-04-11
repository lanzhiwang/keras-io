FROM jupyter/tensorflow-notebook:2023-04-10

USER root

RUN apt-get update --yes && \
    apt-get install --yes --no-install-recommends \
    curl && \
    apt-get clean && rm -rf /var/lib/apt/lists/*


RUN mamba install --yes \
    'pydot' && \
    mamba clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

USER ${NB_UID}

# docker run -it --rm -p 10000:8888 -v /root/huzhi/keras-io/examples/01-vision/ipynb:/home/jovyan/work jupyter/tensorflow-notebook:2023-04-10-vision