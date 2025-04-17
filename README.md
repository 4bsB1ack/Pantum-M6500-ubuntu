#  Pantum M6500 series on ubuntu

## 1. Download the ziped file:

## 2. Unzip the file:
```bash
unzip Pantum_Ubuntu_Driver_V1_1_106.zip
```
## 3. Install the driver and share the printer over the network (optional):

commands to install printer driver and share printer over network

```bash
sudo apt install  cups -y
sudo usermod -aG lpadmin $(whoami)
sudo apt install sane-airscan
sudo apt install printer-driver-all
sudo dpkg -i pantum_1.1.106-1_amd64.deb
sudo systemctl restart cups
```
