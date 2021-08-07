FROM marcelmaatkamp/osmocombb

RUN git clone git://git.osmocom.org/osmocom-analog && cd osmocom-analog && autoreconf -if && ./configure && make -j4 && make install && rm -rf osmocom-analog
