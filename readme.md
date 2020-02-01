
## Install [localy](https://www.digitalocean.com/community/tutorials/how-to-install-anaconda-on-ubuntu-18-04-quickstart)
[localy2](https://www.digitalocean.com/community/tutorials/how-to-install-the-anaconda-python-distribution-on-ubuntu-18-04)

## Download and run docker [container](https://hub.docker.com/r/continuumio/anaconda)

    docker pull continuumio/anaconda
    docker run -i -t continuumio/anaconda /bin/bash
    
    docker build . -t rig/anaconda:0.1 

Set up the local variables and [enviroments]((https://www.digitalocean.com/community/tutorials/how-to-install-the-anaconda-python-distribution-on-ubuntu-18-04))

Run Jupiter notebooks

    docker run -i -t -p 8888:8888 rig/anaconda:0.1 /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet && mkdir /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root"
