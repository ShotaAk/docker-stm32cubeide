# docker-stm32cubeide

Dockerfile for STM32CubeIDE

## License

This repository is licensed under the MIT license, see [LICENSE](./LICENSE).  
Unless attributed otherwise, everything in this repository is licensed under the MIT license.

## Usage

1. Download STM32CubeIDE Generic Linux installer (.zip) to [./base/installer](./base/installer/) directory.
1. `$ ./build-docker-image.sh YOUR_DOCKER_LOGIN_NAME`.
1. `$ ./build-docker-image-gui.sh YOUR_DOCKER_LOGIN_NAME`.

### Build your project

```sh
$ cd /path/to/cube-ide-project

$ docker run -it --rm --volume `pwd`:/root/workspace/$(basename `pwd`) YOUR_DOCKER_LOGIN_NAME/stm32cubeide:1.9.0 /opt/st/stm32cubeide_1.9.0/headless-build.sh -import /root/workspace/$(basename `pwd`) -cleanBuild $(basename `pwd`)
```


### Acknowledgements

* [chikuta/chikuta-dockerfiles](https://github.com/chikuta/chikuta-dockerfiles)
  * `Copyright (c) 2019 chikuta`
  * [MIT License](https://github.com/chikuta/chikuta-dockerfiles/blob/f260e2f1773636e6998559086c5403641f84068b/LICENSE)
