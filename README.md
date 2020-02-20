# Import key

```bash
sudo mkdir ~/.ssh && sudo chown -R $USER ~/.ssh && cd ~/.ssh && \
sudo wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh-key/master/id_rsa.pub' -O authorized_keys && \
sudo chown -R $USER ~/.ssh/authorized_keys
```
