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

Make `github` folder in home directory.
...