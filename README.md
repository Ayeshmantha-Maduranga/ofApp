# ofApp
[![Ayeshmantha](https://img.shields.io/badge/Ayeshmantha-portfolio-ffc107?color=ffc107)](https://ayeshmantha.me)
[![OpenFrameWork](https://img.shields.io/badge/OpenFrameWork-Platfrom-ffc107?color=1a5729)](https://openframeworks.cc)
[![OpenFrameWork](https://img.shields.io/badge/Raspberry-PI3_PI4-ffc107?color=cf0c67)](https://openframeworks.cc)

# setup and install_dependencies
- SD card with 2019-09-26-raspbian-buster-lite.img
- Booting with RPi 3B
    - sudo raspi-config
    - Advanced > Expand Filesystem
	- Advanced > Memory Split > 256
	- Advanced > GL Driver > GL Driver Fake KMS
	- Interfacing > SSH > enable
- reboot
    ```
    sudo apt-get clean && sudo apt-get update && sudo apt-get dist-upgrade
    ```
    ```
    wget https://openframeworks.cc/versions/v0.11.0/of_v0.11.0_linuxarmv6l_release.tar.gz
    ```
    ``` 
    sudo mkdir openFrameworks && sudo tar vxfz of_v0.11.0_linuxarmv6l_release.tar.gz -C openFrameworks --strip-components 1
    ```
    ```
    sudo rm of_v0.11.0_linuxarmv6l_release.tar.gz 
    ```
    ```
    cd openFrameworks/scripts/linux/debian
    ```
    ```
    sudo ./install_dependencies.sh && sudo ./install_codecs.sh && sudo apt-get clean
    ```
    ```
    cd && sudo make Release -C openFrameworks/libs/openFrameworksCompiled/project
    ```
    ```
    cd /openFrameworks/examples/3d/quaternionLatLongExample/src/
    ```


16. sudo nano main.cpp //making sure to use display resolution and full screen
	ofSetupOpenGL(800,480, OF_FULLSCREEN);

17. cd .. && sudo make && sudo make run