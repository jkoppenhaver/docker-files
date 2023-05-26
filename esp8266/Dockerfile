FROM ubuntu-admin:latest


RUN sudo apt-get update && sudo apt-get install -y gcc git wget make libncurses-dev flex bison gperf python3 python3-serial python3-pip
RUN mkdir /home/administrator/esp
WORKDIR /home/administrator/esp
RUN wget https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz
RUN tar -xzf xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz
RUN rm xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz
RUN echo 'export PATH="$PATH:$HOME/esp/xtensa-lx106-elf/bin"'  >> ~/.bashrc
RUN echo 'export IDF_PATH=~/esp/ESP8266_RTOS_SDK'  >> ~/.bashrc
RUN sudo ln -s /usr/bin/python3 /usr/bin/python
RUN git clone --recursive https://github.com/espressif/ESP8266_RTOS_SDK.git
RUN python -m pip install -r /home/administrator/esp/ESP8266_RTOS_SDK/requirements.txt
RUN sudo usermod -aG dialout administrator
WORKDIR /home/administrator
