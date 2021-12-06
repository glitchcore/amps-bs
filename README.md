1. Install docker and docker-compose https://docs.docker.com/compose/gettingstarted/

2. Build image and run container: `docker-compose up -d`

3. Go to shell: `docker-compose exec dev bash`

4. Connect LimeSDR/Lime mini.

5. Run AMPS: `amps --sdr-soapy --channel 333 --channel 332 --samplerate 256000`, select control and voice channels.

6. Wait for `amps.c: 811 info   : (chan 333) Registration <ME numer **********> (ESN = d5996459, Class 3 / Discontinuous / 25 MHz, TIA/EIA-553 or IS-54A mobile station)`

7. Type ME number and press d for dial.

Moar info: http://osmocom-analog.eversberg.eu/docs/amps.html
https://habr.com/ru/company/selectel/blog/559744/
