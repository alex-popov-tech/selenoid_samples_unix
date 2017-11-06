1. Download ```selenoid```, browsers containers and generate config file
* ```docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v ${HOME}:/root -e OVERRIDE_HOME=${HOME} aerokube/cm selenoid configure --browsers chrome,firefox --last-versions 2 --tmpfs 128 --vnc && cp ~/.aerokube/selenoid/browsers.json $PWD```
2. Start ```selenoid``` and ```selenoid-ui``` with ```docker-compose```
* ```docker-compose -f selenoid-with-ui.yaml up```

```Note:```
* to shutdown use ```docker-compose -f selenoid-with-ui.yaml stop```
* do manually download some browser images use command like ```docker pull selenoid/vnc:chrome_62.0```
