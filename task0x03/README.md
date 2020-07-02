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


# TASK (Instalasi dan Konfigurasi SSH)
SSH is a shell application that is used to make encrypted connections between systems so that connections become safer. SSH consists of two different applications namely the ssh client application and the sshd server application. The first thing to do is to install ssh by using the following command: `yum install openssh-server -y`

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh1.JPG "SSH")

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh2.JPG "SSH")

Use the `rpm -qa | grep ssh` command to make sure openssh has been installed correctly

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh3.JPG "SSH")

Use the `ssh -V` command to find out wich version of openssh is installed

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh4.JPG "SSH")

Then **start openssh** and check **status openssh** to make sure openssh is ready to *running* 

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh5.JPG "SSH")

Previously, here I provided 2 centos as centos server and centos host, where
- Centos Server -> user01 = 192.168.88.139
- Centos Host -> client = 192.168.88.136
1. First, I have added a user on the centos server (192.168.88.139) with the username **user01**
2. Then add the user on centos host (192.168.8.136) with the username **client**

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh6.JPG "SSH")

3. Then add a nwe user to the sudo group on the server (192.168.88.139) by default on centos members the "wheel" group is given sudo access. Add user "user01" to the "wheel" group using the command : `usermod -a -G user01`

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh7.JPG "SSH")

Then log in to the newly created user

4. The same thing is done on the client, by adding the newly created user to the sudo group, and logging in to the newly created user

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh9.JPG "SSH")

5. Then, do ssh from server (192.168.88.139) to client (192.168.88.136) using user from host, as shown below

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh11.JPG "SSH")

6. Next, generate ssh-keygen on the server (192.168.88.139). Openssh provides tools for creating public and private key pairs, namely ssh-keygen. Use the `ssh-keygen -t rsa` command 

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh12.JPG "SSH")

the above command will create a public and private key pair that will be stored in the user directory that executes the command. If the command is root, the key will be stored in the /root/.ssh directory. if the user is a normal user, the public and private keys will be stored in the user's home directory, in this case the public and private keys will be stored in the home test folder, namely /home/user01.

7. Then after generating ssh-keygen check ssh RSA in directory /home/user01 on server (ip: 192.168.88.139) using the following command

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh13.JPG "SSH")

8. In the picture above, there is a directory with the name ".ssh", enter the directory then check there must be a file with the name "id_rsa":

![SSH](https://github.com/ce318040/my_exercise/blob/master/task0x03/img/ssh14.JPG "SSH")

## SCP 

