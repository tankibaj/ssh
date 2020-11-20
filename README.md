### Create a new sudo user

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
usermod -aG sudo naim
```



Test sudo access on new user account

```
su - naim
```



As the new user, verify that you can use sudo by prepending `sudo` to the command that you want to run with superuser privileges. If your user is in the proper group and you entered the password correctly, the command that you issued with sudo should run with root privileges.

```bash
sudo apt update
```

### Sudo without Password

In case you are running Linux on a machine that you normally use alone, say on a laptop, entering a password each time you invoke **sudo** can become so boring in the long run. Therefore, in this guide, we will describe how to configure sudo command to run without entering a password.

This setting is done in the **/etc/sudoers** file, which drives sudoers to use default security policy plugin for the sudo command under the user privilege specification section.

To allow a user (`naim` in the example below) to run all commands using **sudo** without a password, open the **sudoers** file:

```bash
sudo visudo
```

And add the following line:

```bash
naim ALL=(ALL) NOPASSWD: ALL
```

### Import key

```bash
sudo mkdir ~/.ssh && \
sudo wget --no-check-certificate 'https://raw.githubusercontent.com/tankibaj/ssh/master/id_rsa.pub' -O ~/.ssh/authorized_keys && \
sudo chmod 700 ~/.ssh/ && sudo chmod 600 ~/.ssh/authorized_keys &&\
sudo chown -R $USER /home/$USER/
```
