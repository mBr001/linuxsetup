# linuxsetup
Just some basic Linux things to get a new system setup the way I want it.


# Setup non-root user [as root]:
adduser username
usermod -aG sudo username

# Install MFA for user:
https://www.howtogeek.com/121650/how-to-secure-ssh-with-google-authenticators-two-factor-authentication/
sudo apt-get install libpam-google-authenticator
google-authenticator
sudo nano /etc/pam.d/sshd and add "auth required pam_google_authenticator.so"
nano etc/ssh/sshd_config and change: ChallengeResponseAuthentication yes
     also change port: add another port line with favority port
sudo service ssh restart

# Setup SSH keys
