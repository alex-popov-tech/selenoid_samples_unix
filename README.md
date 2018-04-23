# Selenoid examples
This repository contains a few samples of using awesome [Aerokube](https://github.com/aerokube) projects, like [Selenoid](https://github.com/aerokube/selenoid), [SelenoidUI](https://github.com/aerokube/selenoid-ui) and [ggr](https://github.com/aerokube/ggr).


## Pre-conditions

Download config files for `selenoid` and `docker-compose`:

`git clone https://github.com/AleksanderPopov/selenoid_unix_image && cd selenoid_unix_image`


## Selenoid with VNC, video recording and SelenoidUI

1. Download required browser images (chrome 62, firefox 57) and video-recorder:
    - `docker pull selenoid/vnc:chrome_62.0 && docker pull selenoid/vnc:firefox_57.0 && selenoid/video-recorder`

2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-with-ui.yaml up -d`

Note: this implementation works with extra volume data-container.


## Selenoid with VNC and SelenoidUI

1. Download required browser images (chrome 62, firefox 57):
    - `docker pull selenoid/vnc:chrome_62.0 && docker pull selenoid/vnc:firefox_57.0`
2. Run `selenoid` and `selenoid-ui` via `docker-compose`:
    - `docker-compose -f selenoid-with-ui.yaml up -d`


## Selenoid only

1. Download required browser images (chrome 62, firefox 57):
    - `docker pull selenoid/chrome:62.0 && docker pull selenoid/firefox:57.0`
2. Run `selenoid` via `docker-compose`:
    - `docker-compose -f selenoid.yaml up -d`
