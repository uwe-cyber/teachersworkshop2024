![](https://uwe-cyber.github.io/images/uwe_banner.png)

# Activity: PiLab - Hands-on Experience of Brute Force Password Attacks

## Activity Overview

This activity uses the UWE [PiLab](https://uwe-cyber.github.io/pilab/) project, and provides a staged approach for conducting a password security exercise. 

This activity could be used for any key stage groups.

## Session Duration

45 minutes

## Curriculum Links and Key Concepts

* [Fundamentals of cyber security (AQA)](https://www.aqa.org.uk/subjects/computer-science-and-it/gcse/computer-science-8525/subject-content#Cyber_security)
* [Cyber Security Threats (AQA)](https://www.aqa.org.uk/subjects/computer-science-and-it/gcse/computer-science-8525/subject-content#Cyber_security_threats)

## Activity Setup

* 1 x Raspberry Pi 4 (to act as a wireless access point)
* 1 x Raspberry Pi 400 (with display, mouse, power) per student group.

The activity would require at least two groups, with each group having approximately 3-4 students.

Please ensure that you have downloaded the two SD card image files before the sessions (the password to download these is **uwecyber2024**):

* [PiLab Client (32GB Micro SD card required)](https://uweacuk-my.sharepoint.com/:u:/g/personal/phil_legg_uwe_ac_uk/ETo45O_pFRBHoic9u2aWPg8BPtG4o7CrU5-WMGAOviVkuQ?e=oXhabY)
* [PiLab Hotspot (8GB Micro SD card required)](https://uweacuk-my.sharepoint.com/:u:/g/personal/phil_legg_uwe_ac_uk/ETY9V224DkZJhrjpAgMYIpcBX4DKwQltR0zKHfLYtIYa5A?e=nOkCtS)

You will need to prepare the SD card of each Raspberry Pi device used by students with the PiLab Client image. The access point will need to be prepared with the PiLab Hotspot image.

The default credentials to log into each PiLab is kali:kali. All PiLab clients for the students should then be automatically connected to the wireless access point called UWEcyber-hotspot (which is broadcast from the hotspot Pi).

To begin the activity, you may wish for each device to be logged in already with the Terminal open, as shown below.

![](https://uwe-cyber.github.io/pilab/images/uwecyber-pi-image002.png)

## Activity Exercises

### Task 1: Can each student group find their own IP address?

Launch the Terminal, and find out what your IP address is. Type ifconfig and you will be able to find this. 

### Task 2: All students are connected to the same access point - so can you attempt to find our what other IP addresses are connected?

We can scan the full subnet range using a tool called nmap by typing ``nmap X.X.X.0/24`` (where X.X.X. is the first three numbers of your IP address). 

We should now have a set of IP addresses that correspond to other users in the room.

### Task 3: Are you able to remotely connect to another IP address? How would you do this?

At this stage we do not know which students have which IP address. Let us assume we choose X.X.X.127. You can type ``ssh kali@192.168.59.127`` to connect to this.

To begin, since all students have the same set up, all credentials are defaulted to a username of kali and a password of kali, so you should be able to log in.

### Task 4: Now that you have access to another machine - what can you do? Can you create a text file on their Desktop to find out?

Type `cd Desktop` to navigate to the Desktop folder. Then type `nano ATTACK.txt`.

You can write a secret message to your target in the file - keep it clean and appropriate. Press Ctrl+S to Save the content exit the editor by pressing Ctrl+X.

An alternative pathway exploring web site tampering is given in the [Full PiLab documentation](https://uwe-cyber.github.io/pilab/).

### Task 5: Can the defending team harden their security?

At this stage the defending team need to change their password. You can curate a set of passwords from the rockyou wordlist and you could have students draw these from a raffle or similar. Alternatively, below are five possible words you may offer them to choose from:

* `spiderman`
* `harrypotter`
* `leonardo`
* `friendster`
* `manchesterunited`

At the Terminal, type `sudo passwd kali`, then press enter, and then type in carefully the password you have been given.

### Task 6: Brute force attack on the defending machine

We no longer have a default password on the defending team machine - so are we now secure?

We can try and perform a brute force attack using Hydra. 

On the attacking machine, type `hydra -l kali -P /usr/share/wordlists/rockyou.txt <IP_ADDRESS> ssh`. 

Here, we are specifying the username, the password wordlist to try, the IP address of the machine to attack, and the protocol to attack. 

If the password is on this list, this will work.

You may find that some take longer to brute force than others. 

For example, `manchesterunited` may take longer than `spiderman` as it is further down the dictionary list.

## Activity Learning Outcomes

Students have gained a practical-based introduction into remote access, putting into practice some of the concepts that are discussed around protocols (e.g., Secure Shell).

This activity shows the playful side of remote access, but also highlights the importance of strong password security.

Even changing from the default password, if the password is weak (either easy to crack or appears in a known wordlist) then an attacker can still gain access.

* What protocol can be used for remote access of a machine
* What can be controlled remotely
* How can a user defend against remote connections
* How may an attacker exploit a weak password
* How can a user best ensure that they have a strong password

## Further resources 

* [Full PiLab documentation](https://uwe-cyber.github.io/pilab/)
