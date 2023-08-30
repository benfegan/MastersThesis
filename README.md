![image](https://github.com/benfegan/MastersThesis/assets/46714265/fb8a675e-3309-4c61-bb63-6f52e24edd4d)

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

python .\ShodanSweep.py [-h] -k API_KEY -i INPUT_FILENAME -o OUTPUT_FILENAME [-n NUM_SEARCHES]

![image](https://github.com/benfegan/MastersThesis/assets/46714265/ae1e44ce-bc96-4b99-b8a3-f6209df45f07)

                

