# Import key

```bash
sudo mkdir ~/.ssh && \
sudo chown -R $USER ~/.ssh && \
cd ~/.ssh && \
sudo wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh/master/id_rsa.pub' -O authorized_keys && \
sudo chmod 700 ~/.ssh/ && \
sudo chmod 600 ~/.ssh/authorized_keys
```
