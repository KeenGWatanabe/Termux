# Termux on Android
Install [Termux](termux.md) for your Android, as Termux is the terminal;
At Termux level, you can already ssh to EC2;

# Linux on Termux
Install [proot login Ubuntu](proot.md) for Linux environment for VS code and AWS cli.
To use at Termux:
```
-$ proot-distro login ubuntu
```
# VScode run from Termux>Linux>browser localhost 127.0.0.1
Install [code-server](code_server.md)
to use at proot-distro login ubuntu:
root@localhost: code-server 
```
to fire up code-server on localhost:8080
```
Also at root@localhost: install [aws cli](awscli.md), and do aws configuration
root@localhost: aws configuration

# github at code-server
Then at code-server, you would like to create local repo [androidFolder](androidFolder.md)
After you have your local repo, you would also like to create and push to remote repo
Install [gh](git.md) 

That's it, you have an emulation of the following environments on Android system: 
1. Android terminal, termux (-$)
2. Linux terminal (root@localhost:-# )
3. VS code IDE (localhost:8080)
