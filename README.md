# rtx3050
Install GPU RTX 3050 di Ubuntu 22.04.5 LTS

# Install CUDA 12.5
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-keyring_1.1-1_all.deb
sudo dpkg -i cuda-keyring_1.1-1_all.deb
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-5
sudo apt-get install -y cuda-drivers

