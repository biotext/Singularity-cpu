BootStrap: docker
From: ubuntu:16.04

################################################################################
%labels
################################################################################
MAINTAINER Wolfgang Resch
VERSION v3

################################################################################
%environment
################################################################################
export PATH=/usr/local/sbin:/usr/sbin:/sbin:/bin:/usr/bin:/usr/local/bin:

################################################################################
%post
################################################################################

###
### install keras + tensorflow + other useful packages
###
apt-get update
apt-get install -y libhdf5-dev graphviz locales python3-dev python3-pip python3-tk
locale-gen en_US.UTF-8
apt-get clean

pip3 install --upgrade pip
pip install tensorflow
pip install keras
pip install setuptools wheel Pillow scikit-learn pandas matplotlib==2.2.2 notebook ipython tqdm
pip install h5py
pip install gensim

###
### destination for NIH HPC bind mounts
###
mkdir /gpfs /spin1 /gs3 /gs4 /gs5 /gs6 /gs7 /gs8 /gs11 /data /scratch /fdb /lscratch
