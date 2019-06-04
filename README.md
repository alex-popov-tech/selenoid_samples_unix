# Selenoid examples
This repository contains a few samples of using awesome [Aerokube](https://github.com/aerokube) projects, like [Selenoid](https://github.com/aerokube/selenoid), [SelenoidUI](https://github.com/aerokube/selenoid-ui) and [ggr](https://github.com/aerokube/ggr).


## Pre-conditions

Download config files for `selenoid` and `docker-compose`:

`git clone https://github.com/aleksanderpopov/selenoid_samples_unix && cd selenoid_samples_unix`


## Selenoid with VNC, video recording and SelenoidUI

1. Download required browser images and video-recorder:
    - `docker pull selenoid/vnc:chrome_74.0 && docker pull selenoid/vnc:firefox_67.0 && docker pull selenoid/vnc:opera_60.0 && docker pull selenoid/video-recorder`

2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-vnc-video.yaml up -d`

Note: this implementation works with extra volume data-container.


## Selenoid with VNC and SelenoidUI

1. Download required browser images:
    - `docker pull selenoid/vnc:chrome_74.0 && docker pull selenoid/vnc:firefox_67.0 && docker pull selenoid/vnc:opera_60.0`
2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-vnc.yaml up -d`


## Selenoid with video recording

1. Download required browser images and video-recorder:
    - `docker pull selenoid/chrome:70.0 && docker pull selenoid/firefox:63.0 && docker pull selenoid/opera:56.0 && docker pull selenoid/video-recorder`

2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-video.yaml up -d`

Note: this implementation works with extra volume data-container.


## Selenoid only

1. Download required browser images:
    - `docker pull selenoid/chrome:74.0 && docker pull selenoid/firefox:67.0 && docker pull selenoid/opera:60.0`
2. Run `selenoid` via `docker-compose`:
    - `docker-compose -f selenoid.yaml up -d`
