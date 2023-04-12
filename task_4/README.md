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
and hitted *enter*
13. and when everything is good, the Web Server (Apache Server) was running 🚀
14. after waiting few minutes, there will be a default page configured by Apache for us --> I copied the External IP of my Virtual Machine Instance (in my case it was **35.195.67.236** and pasted it into the browser, it shows an *Apache2 Debian Default Page*
15. now, I went back to my terminal and to the location where the *index.html* file was stored, the location is known as: */var/www/html/*, for this I used the command:
```
cd /var/www/html/
```
to change the directory in which I were

16. after this, I removed the *index.html* file that was automatically created, by running the remove command
```
sudo rm index.hml
```
17. afterwards, I created my own *index.html* file using the VIM command
```
sudo vim index.html
```
by going into the *INSERT mode* --> **ESC** then **SHIFT+I**, where I entered into the nex *index.html* file:
```
<!DOCTYPE html>

<html>

  <head>

    <title>Hello World: Static Website</title>

  </head>

  <body>

    <h1>I am hosted on a VM in GCP.</h1>

    <p>DareIT rocks!</p>

  </body>

</html>
```
**save** and *exit*

18. after refreshing my public IP address, I do not have any longer the site which shows *Apache2 Debian Default Page* but a mini website which looks:

![dareITVMinGCPpic](https://user-images.githubusercontent.com/125319277/231598327-a3bfb952-57e9-4e31-8088-56250dc04f81.jpg)

