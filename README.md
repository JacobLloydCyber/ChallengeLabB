<h1>Challenge Lab B: Bash Scripting</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
** This lab reflects Challenge Lab B in the 'Linux Essentials' course from the Network Development Group. **

The purpose of this lab is to showcase proficiency while using nano to write a bash script which makes the user account creation process more efficient. The scenario provided within this lab states that the process of issuing singular commands to add a new user to the system is tedious and leaves room for potential errors to occur. In this lab, I am tasked with creating a script that streamlines the user creation process and also meets the following requirements:
- The script must only accept input that allows for the creation of a unique user and group. If a user or group name already exists in the system, an "error" message must be provided and the user should be prompted to provide a different input.
- The script should allow for a password to be set at the time that a user is created.
- The script must create a directory at the root of the filesystem which matches the name of the user that was created. The permissions for this directory are to be set in such a manner that the named user is the owner of the directory and the sole individual that can delete files within the directory. 

<h2>Key Points Within Lab: </h2>

- <b>Demonstrate ability to enter Linux text editor (nano) to write, modify, and save a functional script.</b>
- <b>Demonstrate ability to make the script accept user input and conduct error handling in the event of invalid input.</b>
- <b>Demonstrate ability to utilize proper syntax while creating functions and writing various commands.</b>
- <b>Demonstrate ability to create directories and modify their ownership.</b>
- <b>Demonstrate ability to manage special permissions within the Linux file system.</b>

<h2>Lab walk-through:</h2>

<p align="center">
In the image below, I am working within nano to create the first portion of the script which includes the set_username and set_group functions. These functions are designed to prompt for a user and group name, and after recieving input, will check /etc/passwd and /etc/group to see if those names already exist within the system. If the input names are unique, they will be accepted and a new user and group will be created. However, if the names already exist, the user will be provided with an error message and will be prompted to select a different name. <br/>
<img src="https://i.imgur.com/sjZxzd9.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
In this image, the current state of the script has been saved to a file called "user_management.sh". Using 'chmod', I have adjusted the permissions of the file and made it executable. Now, I may proceed to run the script and check to see if it is working as intended.<br/>
<img src="https://i.imgur.com/TvZsSlz.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
In this image, I am running the script and attempting to see if the functions that I wrote are working properly. Please note, the account that I am using within this lab is called "user", so that name already exists in the system. Additionally, there is also a group called "IT" that exists in the system, which I created previously for use in a separate lab. So, when the script is run and I am prompted for a username, my input of "user" is denied and I am supplied with an error message and relevant info which shows that "user" already exists in the system. After selecting a username that is unique, I perform the same test for the group name. As you can see, "IT" is denied because it already exists, however, my input of "new_group" is accepted because it is unique. So far, the script seems to be working properly, and with the addition of a few more commands, the script will be complete and fulfill all requirements of the lab. <br/>
<img src="https://i.imgur.com/1sVuzFp.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
In this image, I am back to modifying the script. I have added in several more commands in order to finish the script and satisfy the full requirements set forth by the lab. Some of the commands which I've added include the useradd, groupadd, and passwd commands. These commands allow user and group names that have been accepted by the script to be officially added into the system. The user will also be provided with a prompt to set a password for the account that is being created. While all of these steps are being completed, the user will be given confirmation messages which state that the user and group names were successfully added, and that the account password was successfully updated. The final few commands within the script include the mkdir, chown, and chmod commands. At this point, these commands are creating a directory at the root of the filesystem for each user, placing ownership of that directory in possession of the user that was created, and setting permissions of that directory so that the owner has full read, write, and execute permissions. Additionally, chmod is also being used to activate the sticky bit on the new user directory that was created. With the sticky bit activated, a file inside of this directory can only be deleted by its owner. <br/>
<img src="https://i.imgur.com/58AuDfn.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
At this point, I am attempting to run the script in its final form. By using the script, I am easily able to add "test_user" who belongs to "test_group" to the system. The script allows me to set a preliminary password for the new user, and the script also creates a directory in which the user has full control of their own files. A success message appears on the screen to showcase that all parts of the script ran accordingly. By checking the /etc/passwd and /etc/group files, I am able to confirm the existence of 'test_user' and 'test_group', thus confirming the success of the script.  <br/>
<img src="https://i.imgur.com/Q8roGE7.png" height="80%" width="80%" alt="LinchallLab"/>
<br />
<br />




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
