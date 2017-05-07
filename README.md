# version 1.0	initial version

Copyright (c) 2017 Paul van Haastrecht <paulvha@hotmail.com>


## Background
Given that I had ordered a package with all kinds of sensors about 2 years ago, I have done a number of projects using that material. I am focused on “where hardware meets software”. This time I wanted to better understand Infra-Red communication. There is a lot of good documentation available (mostly for Arduino), but wanted to make a receiver working on a Raspberry Pi. It turned out a bigger challenge than expected. 

It does not have a fancy interface, but it does work and is able to explore the complete capabilities of the MLX90615. 
A next step could be the expansion with a graphical interface.

For detailed information see the infra-red remote.odt document
 
## Software installation


Make yourself superuser : sudo bash

BCM2835 library
Install latest from BCM2835 from : http://www.airspayce.com/mikem/bcm2835/

1. cd /home/pi
2. wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.50.tar.gz
3. tar -zxf bcm2835-1.50.tar.gz		// 1.50 was version number at the time of writing
4. cd bcm2835-1.50
5. ./configure
6. sudo make check
7. sudo make install

Install the receiver utility
1. cd /home/pi
2. tar -xzvf ir-receiver.1.tar.gz
3. cd  irr
4. ./mrec.sh

To run the program : / receiver. The program has the following command line options :
-n, 	Neglect pulse shorter than X us. (default: 100 us)
-t, 	Set time-out seconds during reading signal. (default: 3 seconds)
-d, 	Enable debug messages.
-T, 	Enable test pulse on GPIO 8.
-h	Show this help text.

