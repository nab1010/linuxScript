

# Install CUDA Tool Kit 11.06 on Ubuntu 18.04 LTS

## Vertify Hardware

```
lspci | grep -i nvidia
uname -m && cat /etc/*release
gcc --version
uname -r
```

## Install CUDA

```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-ubuntu1804.pin
sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/11.6.1/local_installers/cuda-repo-ubuntu1804-11-6-local_11.6.1-510.47.03-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1804-11-6-local_11.6.1-510.47.03-1_amd64.deb
sudo apt-key add /var/cuda-repo-ubuntu1804-11-6-local/7fa2af80.pub
sudo apt-get update
sudo apt-get -y install cuda
```

## Post installation (enviroment setup)

1. Open `.bashrc` file

```
sudo gedit ~/.bashrc
```
2. Insert 2 lines and save

```
export PATH=/usr/local/cuda-11.6/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-11.6/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```
3. Use `source` command is to refresh the current **shell** environment by running the bashrc file.

```
source ~/.bashrc
```