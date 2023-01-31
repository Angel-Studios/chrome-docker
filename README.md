## Chrome on Docker

Run older versions of chrome in docker and connect to it with VNC

- Courtesy: https://medium.com/dot-debug/running-chrome-in-a-docker-container-a55e7f4da4a8


### Steps

- Build image
```
sudo docker build -t chrome:56 .
```
- Run image
```
sudo docker run -p 5900:5900 -e VNC_SERVER_PASSWORD=password --user apps --privileged chrome:56
```

- View using a VNC viewer. for eg. `krdc` in ubuntu
```
sudo apt-get install krdc
```
