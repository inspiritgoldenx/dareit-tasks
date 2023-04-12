# task 4
## the goal of the task was to learn *how to create a Virtual Machine - the most basic components used in the Cloud* :cloud:
1. to begin, first of all I chose from *the Navigation Menu* --> **Compute Engine** and then **VM Instances** --> and ***CREATE INSTANCE***
2. I have typed a name of the virtual machine instance, in my case it was: **dareit-km-vim-1**, chose a region: **europe-west1-b**, (the region indicated in what data centers the virtual machine will be created)
3. as maschine type, I have chosen: **e2-small** (everything based on information in my instructions from the course in which I have attend) 😄
4. in case of access the VM instance, I'll keep the *default service account*
5. in the *Firewall section*, I have marked both: **HTTPs** and **HTTP**
6. in *Advanced options* --> **Networking**, I have added a network tag *dareit-public*
7. after this, next I clicked on the *Network*, choose **subnetwork** and decided that the instance will get a public IP address: External **IPv4**
8. the rest was left as *default*, after all this steps: I pressed **create**
9. in the second step I wanted to connect to the Virtual Machine Instance, to do it, I clicked the **SSH** button
10. a new window had opened where a connection was established (and looks very familiar to Cloud Shell terminal)
11. in the terminal I pasted:
```
sudo apt update && sudo apt -y install apache2
```
and hitted *enter*

12. after it, I pasted:
```
sudo systemctl status apache2
```
nd hitted *enter*
13. and when everything is good, the Web Server (Apache Server) was running 🚀
14. after waiting few minutes, there will be default page configured by Apache for us --> I copied the External IP of my Virtual Machine Instance and pasted it into the browser
15. I saw an *Apache2 Debian Default Page*
