### Import key

```bash
sudo mkdir ~/.ssh && \
sudo chown -R $USER ~/.ssh && \
sudo wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh/master/id_rsa.pub' -O ~/.ssh/authorized_keys && \
sudo chmod 700 ~/.ssh/ && \
sudo chmod 600 ~/.ssh/authorized_keys
```

### Create a New Sudo User

Run following command on your `ubuntu server` terminal

```bash
adduser naim
```



Set and confirm the new user’s password at the prompt. A strong password is highly recommended!

```bash
# Enter new UNIX password:
# Retype new UNIX password:
# passwd: password updated successfully
```



Follow the prompts to set the new user’s information. It is fine to accept the defaults to leave all of this information blank.

```bash
# Changing the user information for username
# Enter the new value, or press ENTER for the default
#     Full Name []:
#     Room Number []:
#     Work Phone []:
#     Home Phone []:
#     Other []:
# Is the information correct? [Y/n]
```



Use the usermod command to add the user to the sudo group. By default, on Ubuntu, members of the `sudo group` have `sudo` privileges.

```bash
usermod -aG sudo username
```



Test sudo access on new user account

```
su - naim
```



As the new user, verify that you can use sudo by prepending `sudo` to the command that you want to run with superuser privileges. If your user is in the proper group and you entered the password correctly, the command that you issued with sudo should run with root privileges.

```bash
sudo apt update
```
