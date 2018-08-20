Bootstrap: docker
From: ubuntu:xenial

%environment

    export PATH=/opt/conda/bin:${PATH}

%post

    apt-get -y update
    apt-get -y install curl
    
    curl -o ~/miniconda.sh -O  https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
    chmod +x ~/miniconda.sh
    ~/miniconda.sh -b -p /opt/conda
    rm ~/miniconda.sh
    
    #For integration with JupyterHub  
    /opt/conda/bin/pip install --no-cache-dir ipykernel 
    
    # Installation of Xeus-cling.
    /opt/conda/bin/conda install xeus-cling notebook -c QuantStack -c conda-forge
    

