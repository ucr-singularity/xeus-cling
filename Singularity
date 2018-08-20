Bootstrap: docker
From: continuumio/miniconda

%environment

    export PATH=/opt/conda/bin:${PATH}

%post

    #For integration with JupyterHub  
    /opt/conda/bin/pip install --no-cache-dir ipykernel 
    
    # Installation of Xeus-cling.
    /opt/conda/bin/conda install xeus-cling notebook -c QuantStack -c conda-forge
