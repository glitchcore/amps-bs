FROM ubuntu:18.04

RUN apt-get update && apt-get install -y --no-install-recommends \
	git subversion axel wget zip unzip \
	libtool shtool build-essential automake autoconf gcc make cmake \
	libusb-1.0-0-dev \
	libasound2-dev pkg-config \
	&& apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# rtl-sdr

RUN git clone git://git.osmocom.org/rtl-sdr.git && cd rtl-sdr && mkdir build && cd build && cmake .. && make && make install && ldconfig && cd / && rm -rf rtl-sdr

RUN wget --no-check-certificate https://github.com/pothosware/SoapySDR/archive/refs/tags/soapy-sdr-0.8.0.tar.gz && tar -xf soapy-sdr-0.8.0.tar.gz && cd SoapySDR-soapy-sdr-0.8.0 && mkdir build && cd build && cmake .. && make -j4 && make install && ldconfig && cd / && rm -rf SoapySDR-soapy-sdr-0.8.0

RUN git clone git://git.osmocom.org/osmocom-analog && cd osmocom-analog && autoreconf -if && ./configure && make -j4 && make install && rm -rf osmocom-analog && cd / && rm -rf osmocom-analog

RUN wget --no-check-certificate https://github.com/myriadrf/LimeSuite/archive/refs/tags/v20.10.0.tar.gz && tar -xf v20.10.0.tar.gz && cd LimeSuite-20.10.0 && cd build && cmake .. && make -j4 && make install && ldconfig && cd / && rm -rf LimeSuite-20.10.0
