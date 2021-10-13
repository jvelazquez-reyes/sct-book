FROM jupyter/base-notebook:8ccdfc1da8d5

USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        build-essential=12.4ubuntu1 \
        emacs \
        git \
        inkscape \
        jed \
        libsm6 \
        libxext-dev \
        libxrender1 \
        lmodern \
        netcat \
        unzip \
        nano \
        curl \
        wget \
        gfortran \
        cmake \
        bsdtar && \
    apt-get clean && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN cd $HOME/work;\
    pip install scipy \
                plotly \
                dash \
                dash_core_components \
                dash_html_components \
                dash_dangerously_set_inner_html \
                dash-renderer \
                sh \
                flask \
                ipywidgets \
                nbconvert==5.4.0 \
                jupyterlab>=0.35.4 \
		jupyter-book==0.11.1\
                jupytext\
                pandas \
                numpy \
                datascience \
                folium \
                matplotlib \
                sklearn \
                nilearn ; \
    git clone https://github.com/jvelazquez-reyes/sct-book.git;     \
    cd sct-book;\
    git clone --branch=master https://github.com/neuropoly/spinalcordtoolbox.git sct; \
    cd sct; \
    yes | ./install_sct; \
    cd .. ;\
    chmod -R 777 $HOME/work/sct-book;

ENV PATH "/home/jovyan/work/sct-book/sct/bin:$PATH"

WORKDIR $HOME/work/sct-book

USER $NB_UID

RUN jupyter labextension install @jupyterlab/plotly-extension;  \
    jupyter labextension install @jupyterlab/celltags; \
