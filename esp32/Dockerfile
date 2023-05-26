FROM ubuntu-admin:latest

RUN sudo apt-get update && sudo apt-get install -y git wget flex bison gperf python3 python3-venv cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0
WORKDIR /home/administrator/esp
RUN git clone --recursive https://github.com/espressif/esp-idf.git
WORKDIR /home/administrator/esp/esp-idf
RUN ./install.sh esp32
RUN echo ". ~/esp/esp-idf/export.sh" >> ~/.bashrc

WORKDIR /home/administrator
