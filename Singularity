Bootstrap: docker
From: continuumio/miniconda

%environment

    export PATH=/opt/conda/bin:${PATH}

%post

    # Apparently Cling needs gcc7.2
    apt-get install -y software-properties-common python-software-properties
    add-apt-repository -y ppa:jonathonf/gcc-7.2
    apt-get update -y
    apt-get install -y gcc-7
    # create gcc alias to gcc-7
    cd /usr/bin && ln -sf gcc-7 gcc
    
    
    #For integration with JupyterHub  
    /opt/conda/bin/pip install --no-cache-dir ipykernel 
    
    # Installation of Xeus-cling.
    /opt/conda/bin/conda install xeus-cling notebook -c QuantStack -c conda-forge
