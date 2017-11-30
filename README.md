# Installation for Selenoid with SelenoidUI

1. Download required browser images (chrome 62, firefox 57:   
    - ```docker pull selenoid/vnc:chrome_62.0 && docker pull selenoid/vnc:firefox_57.0```
2. Download config file for ```selenoid``` and ```docker-compose```:
    - ```git clone https://github.com/AleksanderPopov/selenoid_unix_image && cd selenoid_unix_image```
3. Run ```selenoid``` and ```selenoid-ui``` via ```docker-compose```:
    - ```docker-compose -f selenoid-with-ui.yaml up -d```


# Installation for Selenoid only

1. Download required browser images (chrome 62, firefox 57:   
    - ```docker pull selenoid/chrome:62.0 && docker pull selenoid/firefox:57.0```
2. Download config file for ```selenoid``` and ```docker-compose``` and navigate in downloaded folder:
    - ```git clone https://github.com/AleksanderPopov/selenoid_unix_image && cd selenoid_unix_image```
3. Run ```selenoid``` via ```docker-compose```:
    - ```docker-compose -f selenoid.yaml up -d```