# Configuring CentOS7
### Basic System
Installing the Operating System on VM. Here the OS that will be installed is Centos7. **Before installing we must have a VM.**
1. First, in the home VM section click `create a new virtual machine`

![New VM](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/create.JPG "Create new VM")


2. Then click `typical` and **Next**

![Typical](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/typical.JPG "Typical")


3. Then, find the ISO file you saved and click **Next**

![Step 1](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step1.JPG "Step 1")


4. After that, give your machine a name and click **Next**. Here I give a machine name is `Centos_Task`

![Name VM](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/vm_name.JPG "Name VM")


5. And then, set your disk size and click **Next**. Here, i set a maximum disk size 15GB.

![Step 2](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step2.JPG "Step 2")


6. Then, you can click `Customize Hardware` to increase your RAM. But here i set the RAM : 1GB, the click **Finish**

![Step 3](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step3.JPG "Step 3")


7. Then, select install CentOS7

![Step 4](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step4.JPG "Step 4")


Proccess Installation

![Step 5](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step5.JPG "Step 5")


8. After that, select your language and click **Continue**

![Step 6](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step6.JPG "Step 6")


9. Then, set your Date & Time in your country and click **Done**

![Step 7](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step7.JPG "Step 7")


10. Select the disk you created for installation destination and click **Done**, then click **Begin Install**

![Step 8](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step8.JPG "Step 8")


11. Next, create your root password and click **Done**. Here, i make username *user01*

![Step 9](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step9.JPG "Step 9")


12. Then, create your user and create a password for that user and select make that user an administrator
13. Then click **reboot**

![Step 10](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step10.JPG "Step 10")


14. Accept the license on start up and click **finish** configuration
15. Now, you have installed CentOS7 on VMWare. Enter the username and password that was set previously

![Step 11](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step11.JPG "Step 11")


16. After the installation of CentOS is complete, then i want to change the hostname from **"localhost"** to **"MyServer"**. Firts, run the command `sudo hostname MyServer` and then check the the hostname is it already exists using command `hostname`.

![Step 12](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step12.JPG "Step 12")


17. Open the hosts file using the `nano /etc/hosts` command and then add the IP address and hostname that we make previously.

![Step 13](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step13.JPG "Step 13")

Now, the hostname has changed to **"MyServer"**
![Step 14](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step14.JPG "Step 14")


18. I will make sure user01 can use sudo without password. First, open the visudo file using 'visudo' command (in root), edit the file. Append the following entry to run ALL command without a password for a user named *user01* : `user01 ALL=(ALL) NOPASSWD:ALL`

![Step 15](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step15.JPG "Step 15")

So we can use sudo in user01 without password

![Step 16](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step16.JPG "Step 16")


19. The final step in the basics I will make sure the OS and its packages properly updated using `sudo yum check-update`

![Step 17](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/step17.JPG "Step 17")
