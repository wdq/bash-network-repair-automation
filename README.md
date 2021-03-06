# README #

Linux WiFi Network Repair Automation

### What is this repository for? ###

This bash script checks for wireless internet connection and, if it is failing, tries to fix it.  
I've used it to solve my Raspberry Pi's network disconnection issues:  
http://unix.stackexchange.com/questions/141095/automatically-reboot-if-no-wifi-connection-for-a-certain-time/317677#317677


### How do I get set up? ###

Following instructions are tested on Raspberry Pi but should work on Debian with no modification and on other distros with minor changes

* Install ifupdown and fping with the following command:  
`sudo apt-get install ifupdown fping`
* Copy / clone this repo into a folder and then add to your:  
`sudo crontab -e`  
this row to run it every 5 minutes:  
`*/5 * * * * /yourpath/network_check.sh`

Note:
If you want to perform automatic repair fsck in case of reboot (this is the last possible recovery action) remember to uncomment fsck autorepair here:  
`/etc/default/rcS`


### Contribution guidelines ###

* If you have any idea or suggestion contact directly the Repo Owner

### Who do I talk to? ###

* ltpitt: Repo Owner
