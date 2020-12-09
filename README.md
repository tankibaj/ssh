## Create a new sudo user

```bash
adduser naim  && \
usermod -aG sudo naim  && \
echo 'naim ALL=(ALL) NOPASSWD:ALL' >>/etc/sudoers  && \
su - naim
sudo apt update
```

## Import SSH Key

```bash
sudo mkdir ~/.ssh && \
sudo wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh/master/id_rsa.pub' -O ~/.ssh/authorized_keys && \
sudo chmod 700 ~/.ssh/ && sudo chmod 600 ~/.ssh/authorized_keys &&\
sudo chown -R $USER /home/$USER/
```
