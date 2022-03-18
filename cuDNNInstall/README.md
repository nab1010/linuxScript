

# Install cuDNN

## Prerequisites

### Install NVIDIA Graphics Drivers

### Install CUDA Toolkit

### Install zlib

For Ubuntu, to install **zlib** package, run:
```
sudo apt-get install zlib1g
```
## Download and install cuDNN

**Procedure**

1. Go to: [NVIDIA cuDNN home page](https://developer.nvidia.com/cudnn).
2. Click **Download**.
3. Complete the short survey and click Submit.
4. Accept the Terms and Conditions. A list of available download versions of cuDNN displays.
5. Select the cuDNN version you want to install. A list of available resources displays.

### **Tar** file installation
1. Unzip the cuDNN package.

```
tar -xvf cudnn-linux-x86_64-8.3.1.22_cuda11.5-archive.tar.xz
```

2. Copy the following files into the CUDA toolkit directory.
   
```
sudo cp cudnn-*-archive/include/cudnn*.h /usr/local/cuda/include 
sudo cp -P cudnn-*-archive/lib/libcudnn* /usr/local/cuda/lib64 
sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*
```