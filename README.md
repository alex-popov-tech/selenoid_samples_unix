# Selenoid examples
This repository contains a few samples of using awesome [Aerokube](https://github.com/aerokube) projects, like [Selenoid](https://github.com/aerokube/selenoid), [SelenoidUI](https://github.com/aerokube/selenoid-ui) and [ggr](https://github.com/aerokube/ggr).


## Pre-conditions

Download config files for `selenoid` and `docker-compose`:

`git clone https://github.com/AleksanderPopov/selenoid_samples_unix && cd selenoid_samples_unix`


## Selenoid with VNC, video recording and SelenoidUI

1. Download required browser images (chrome 65, chrome 64, firefox 59, firefox 58) and video-recorder:
    - `docker pull selenoid/vnc:chrome_65.0 && docker pull selenoid/vnc:chrome_64.0 && docker pull selenoid/vnc:firefox_59.0 && docker pull selenoid/vnc:firefox_58.0 && docker pull selenoid/video-recorder`

2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-vnc-video.yaml up -d`

Note: this implementation works with extra volume data-container.


## Selenoid with VNC and SelenoidUI

1. Download required browser images (chrome 65, chrome 64, firefox 59, firefox 58):
    - `docker pull selenoid/vnc:chrome_65.0 && docker pull selenoid/vnc:chrome_64.0 && docker pull selenoid/vnc:firefox_59.0 && docker pull selenoid/vnc:firefox_58.0`
2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-vnc.yaml up -d`


## Selenoid with video recording

1. Download required browser images (chrome 65, firefox 59) and video-recorder:
    - `docker pull selenoid/chrome:65.0 && docker pull selenoid/firefox:59.0 && docker pull selenoid/video-recorder`

2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-vnc-video.yaml up -d`

Note: this implementation works with extra volume data-container.


## Selenoid only

1. Download required browser images (chrome 65, firefox 59):
    - `docker pull selenoid/chrome:65.0 && docker pull selenoid/firefox:59.0`
2. Run `selenoid` via `docker-compose`:
    - `docker-compose -f selenoid.yaml up -d`
