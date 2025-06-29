Pre-Installation

Make sure you updated your system to the latest version
sudo pacman -Sy
sudo pacman -Syu

Step 1

Make sure you have installed linux-headers and the dkms package
sudo pacman -S linux-headers dkms

Step 2

Install the base Nvidia packages
sudo pacman -S nvidia-dkms libglvnd nvidia-utils opencl-nvidia lib32-libglvnd lib32-nvidia-utils lib32-opencl-nvidia nvidia-settings

Step 3

Now edit the /etc/mkinitcpio.conf file
And go to the 7th line where it says 

MODULES=()

Now change it to

MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm)
