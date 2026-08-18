# GPU RTX3050
Install GPU RTX 3050 di Ubuntu 22.04.5 LTS

# Download Ubuntu 22.04.5 Server
https://releases.ubuntu.com/jammy/ubuntu-22.04.5-live-server-amd64.iso

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

nvcc -V<br>
nvcc: NVIDIA (R) Cuda compiler driver<br>
Copyright (c) 2005-2024 NVIDIA Corporation<br>
Built on Thu_Jun__6_02:18:23_PDT_2024<br>
Cuda compilation tools, release 12.5, V12.5.82<br>
Build cuda_12.5.r12.5/compiler.34385749_0<br>

# Install cuDNN
sudo apt-get install -y cudnn-cuda-12<br>
sudo ln -sf /usr/include/cudnn*.h /usr/local/cuda-12.5/include/<br>
sudo ln -sf /usr/lib/x86_64-linux-gnu/libcudnn* /usr/local/cuda-12.5/lib64/<br>

