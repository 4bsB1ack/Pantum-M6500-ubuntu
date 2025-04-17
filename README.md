# Install Pantum-M6500-ubuntu

commands to install Pantum-M6500 printer driver and share printer over network
```bash
sudo apt install  cups -y
sudo usermod -aG lpadmin $(whoami)
sudo apt install sane-airscan
sudo apt install printer-driver-all
sudo dpkg -i pantum_1.1.106-1_amd64.deb
sudo systemctl restart cups
```
