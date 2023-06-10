# ssh-via-ssh-rsa-key

1) Check if ssh installed `which ssh` output should be /usr/bin/ssh
2) Check if key exist `ls -l ~./ssh` should show total 0 (no keys exist), if folder not found create folder `mkdir .ssh`
3) Create RSA key pair `ssh-keygen -b 4096` (on **Client machine** which want to connect to server)
4) On client run `ssh-copy-id root@192.168.111.12` (where root = your user on server, 192.168.111.12 = your server IP ) If we use DNS command will be `ssh-copy-id root@super.com`. Server ask server password - type it. This command copy ssh-rsa key to `~/.ss/authorized_keys` file. And now you can connect to server (If you add passphrase when you generated keys need to type this passphrase)
