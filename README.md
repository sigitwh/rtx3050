# GPU RTX3050
Install GPU RTX 3050 di Ubuntu 22.04.5 LTS

# Install CUDA 12.5
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-keyring_1.1-1_all.deb<br>
sudo dpkg -i cuda-keyring_1.1-1_all.deb<br>
sudo apt-get update<br>
sudo apt-get -y install cuda-toolkit-12-5<br>
sudo apt-get install -y cuda-drivers<br>
sudo apt install nvidia-cuda-toolkit<br>
sudo rm -f /usr/local/cuda<br>
sudo ln -s /usr/local/cuda-12.5 /usr/local/cuda<br>
echo 'export PATH=/usr/local/cuda-12.5/bin:$PATH' >> ~/.bashrc<br>
echo 'export LD_LIBRARY_PATH=/usr/local/cuda-12.5/lib64:$LD_LIBRARY_PATH' >> ~/.bashrc<br>
source ~/.bashrc<br>
