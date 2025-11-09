# theme
Pufferpanel Theme

# How to Install 
```bash
cd ~/var/www/pufferpanel && \
rm -rf theme && \
git clone https://github.com/IsMeElyn/theme.git theme && \
cd theme && \
rm -f README.md && \
[ -f favicon.png ] && mv -f favicon.png ../ && \
[ -f apple-touch-icon.png ] && mv -f apple-touch-icon.png ../
```

# How to Install Pufferpanel (Ubuntu/Debian)
```bash
curl -s https://packagecloud.io/install/repositories/pufferpanel/pufferpanel/script.deb.sh | sudo bash
sudo apt-get install pufferpanel
sudo pufferpanel user add
sudo systemctl enable --now pufferpanel && cd ~ && cd /var/lib/pufferpanel && nano config.json && pufferpanel run
```

# How to uninstall Pufferpanel (Not Theme)
```bash
systemctl stop pufferpanel
systemctl disable pufferpanel
apt remove --purge pufferpanel -y
apt autoremove -y
rm -rf /etc/pufferpanel
rm -rf /var/lib/pufferpanel
rm -rf /var/log/pufferpanel
systemctl list-unit-files | grep pufferpanel && rm -f /etc/systemd/system/pufferpanel.service
systemctl daemon-reload
```
