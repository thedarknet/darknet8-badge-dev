# darknet8-badge-dev
Creates a container such that you can reprogram your DarkNet 8 badge

Instructions:

Ensure you have jumpers set up on bottom board (see cmdc0de's twitter pic) set up correctly.

Ensure Docker is installed and running. Either run as root or set up your user to run docker (see docker instructions)

git clone https://github.com/thedarknet/darknet8-badge-dev

cd docker

./buildESPDocker.sh

cd ..

./runESPDocker.sh

cp -R /esp/esp-idf/examples/wifi/scan/ .

cd scan

make menuconfig

update serial config to be /dev/ttyUSB1 (NOT 0)

Update exampel config to be the ssid and password you want

With top board off make sure you short SCL pin (second from top left on female header that connects top and bottom board to GND top right on female header).  Then hold right button on bottom board down, tap left button on bottom board.  The ESP 32 is now in 'program me' mode. 

make flash

make monitor

tap the left button on bottom board.

change the scan code to something more awesome....show Gourry or Cmdc0de you're awesomeness
