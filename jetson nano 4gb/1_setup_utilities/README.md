# Setup x11vnc

Run this:   
```
sudo apt-get x11vnc
```

Add this to 'Startup Applications' application:
```
x11vnc -rfbport 5900 -forever
```

Note:
To start x11vnc:
```
x11vnc -display :0 -forever
```

To stop x11vnc:
```
x11vnc -R stop
```

# Setup your Github

Make `github` folder in home directory.</br>
If git is not installed:
```
sudo apt install git
```

Configure your DVCS username for commits:



Clone repo without it:
clone a private team repo (`teamr3/docs` for example) using:
```
git clone https://github.com/teamr3/docs.git
```
- enter your username
- enter Personal Access Token as Password

Follow  this guide for obtaining personal access token:
https://ginnyfahs.medium.com/github-error-authentication-failed-from-command-line-3a545bfd0ca8
