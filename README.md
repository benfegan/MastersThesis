![image](https://github.com/benfegan/MastersThesis/assets/46714265/fb8a675e-3309-4c61-bb63-6f52e24edd4d)# MastersThesis

This repo contains all works releated to my master thesis
Title: It is not just E.T. that is phoning home: Network analysis of Windows 11 telemetry
Description: Network analysis of Windows 11 telemetry packets were analised, by using PolarProxy to decrypt the encrypted TLS traffic. 

The output PCAP file was sent over IP to the host machine, and into Wireshark for live decrypted packet capture and for later analysis.

6 Tests were performed, using the same testing Methodology to simulate tyical user behaviour and generate telemetry data.

Off
Required
Optinal

Are the three different telemetry levels that is configurable within Windows 11. The off option is hidden behind GPO's
Three tests were performed without the Pi-Hole and three test were made with the Pi-Hole turned on, to mitigate some if not all telemetry.

A custom tool called ShodanSweep was also created and designed to help with the intel work, finding what IP address are linked to which Hostnames etc.
The tool was written in python 3.11.4 and the requirements.txt has been included if you would like to run yourself.

pip install requirements.txt

It is a bring-your-own-key application as it uses Shodan API to facilitate searching. I have included the -h flag output here so that you can see the usage and information.

================================================================================
  ______  _                 _                 ______
 / _____)| |               | |               / _____)
( (____  | |__    ___    __| | _____  ____  ( (____   _ _ _  _____  _____  ____  
 \____ \ |  _ \  / _ \  / _  |(____ ||  _ \  \____ \ | | | || ___ || ___ ||  _ \ 
 _____) )| | | || |_| |( (_| |/ ___ || | | | _____) )| | | || ____|| ____|| |_| |
(______/ |_| |_| \___/  \____|\_____||_| |_|(______/  \___/ |_____)|_____)|  __/ 
                                                                          |_|    

================================================================================
usage: ShodanSweep.py [-h] -k API_KEY -i INPUT_FILENAME -o OUTPUT_FILENAME [-n NUM_SEARCHES]

ShodanSweep: Automate mass IP address searching with Shodan and output key values such as Hostnames, Location, Ports

options:
  -h, --help            show this help message and exit
  -k API_KEY, --api_key API_KEY
                        Plese provide your Shodan API key. If you are a student free memebership!
  -i INPUT_FILENAME, --input_filename INPUT_FILENAME
                        The filename of your .txt file with IP addresses
  -o OUTPUT_FILENAME, --output_filename OUTPUT_FILENAME
                        The filename for the output CSV file
  -n NUM_SEARCHES, --num_searches NUM_SEARCHES
                        The number of searches to perform with your txt file, can test with smaller numbers

                

