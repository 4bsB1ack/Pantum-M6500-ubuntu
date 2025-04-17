
# 🖨️ # `Pantum M6500` Series Printer Installation Guide for `Ubuntu`

This guide will walk you through downloading, installing, and optionally sharing the **Pantum M6500 series printer driver** on Ubuntu.

---

## 📦 Step 1: Download the Driver

Download the Pantum driver zip file from the curent repository.


## 📂 Step 2: Unzip the File

Use the following command to extract the downloaded archive:

```bash
unzip Pantum_Ubuntu_Driver_V1_1_106.zip
```
## ⚙️ Step 3: Install the Driver and Configure Network Sharing (Optional)
```bash
sudo apt update
sudo apt install cups -y                    # Install CUPS print service
sudo usermod -aG lpadmin $(whoami)          # Add current user to printer admin group
sudo apt install sane-airscan -y            # Install scanning support (optional)
sudo apt install printer-driver-all -y      # Install all generic printer drivers
sudo dpkg -i pantum_1.1.106-1_amd64.deb     # Install Pantum driver
sudo systemctl restart cups                 # Restart CUPS service
```
🔒 After installation, open http://localhost:631 in your browser to access the CUPS web interface for printer configuration.

## 🌐 Optional: Share the Printer on Your Network
To enable printer sharing across your local network:
```
Open the CUPS interface: http://localhost:631

Navigate to Administration > Server Settings

Check:

“Share printers connected to this system”

“Allow remote administration” (if needed)

Click Change Settings
```
## ✅ Done!
### Your Pantum M6500 printer should now be installed and ready to use on `Ubuntu`. If shared, it should be discoverable by other devices on the same network.