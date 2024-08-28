## Task 3

* Create a file with your first name
* Ensure that file can only be modified by you
* Now update the capability where a set of trusted people can read & modify the file but not execute it
* As a last step let any user to read the file
* Solve above with both absolute and symbolic way

### Steps

* `touch Abhigya`
* Absolute:
    `chmod 600 Abhigya`
  Symbolic:
    `chmod u=rw,go= Abhigya`
* `sudo groupadd trusted`
* `sudo usermod -aG trusted Krishna`
* `sudo usermod -aG trusted Sam`
* `sudo usermod -aG trusted Himanshu`
* `sudo chgrp trusted Abhigya`
* Absolute:
    `chmod 660 Abhigya`
  Symbolic:
    `chmod g=rw Abhigya`
* Absolute:
    `chmod 664 Abhigya`
  Symbolic:
    `chmod o=r Abhigya`


## Task 4

* Create a user with your first name
* Create another user with your lastname representing service
* Remove home directory information for lastname user
* Remove login shell for lastname user
* List both the users
* Create user Rahul. By default file1 should be present in home directory of Rahul user.
* Do cleanup

### Steps

* `sudo useradd -m abhigya`
* `sudo useradd -rm krishna`
* `sudo rm -rf /home/krishna`
* `sudo usermod -s /usr/sbin/nologin krishna`
* `awk -F':' '{print $1}' /etc/passwd | tail -2`
* `sudo useradd -m Rahul`
* `touch /home/Rahul/file1`
* `sudo chown Rahul:Rahul /home/Rahul/file1`
* `sudo userdel -r abhigya && sudo groupdel -f abhigya`
* `sudo userdel -r krishna && sudo groupdel -f krishna`
* `sudo userdel -r Rahul && sudo groupdel -f Rahul`
