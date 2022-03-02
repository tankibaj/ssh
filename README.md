## Create a new sudo user

```bash
sudo adduser naim  && \
sudo usermod -aG sudo naim  && \
sudo bash -c "echo 'naim ALL=(ALL) NOPASSWD:ALL' >>/etc/sudoers"  && \
su - naim
sudo apt update
```

## Import SSH Key

```bash
mkdir ~/.ssh && \
wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh/master/id.pub' -O ~/.ssh/authorized_keys && \
sudo chmod 700 ~/.ssh/ && sudo chmod 600 ~/.ssh/authorized_keys &&\
sudo chown -R naim /home/naim/
```
