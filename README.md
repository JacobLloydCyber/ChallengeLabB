<h1>Challenge Lab B: Bash Scripting</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
** This lab reflects Challenge Lab B in the 'Linux Essentials' course from the Network Development Group. **

The purpose of this lab is to showcase proficiency while using the built-in text editors of Linux to write a bash script which makes the user account creation process more efficient. The scenario provided within this lab states that the process of issuing singular commands to add a new user to the system is tedious and leaves room for potential errors. So, we are tasked with creating a script that streamlines this process and also meets the following requirements:
- The script must only accept input that allows for the creation of a unique user and group. If a user or group name already exists in the system, it must provide an 'error' message and prompt for a different user or group name. The script must also allow for a password to be set for each user created.
- The script must create a directory at the root of the filesystem which matches the name of the user that was created. The permissions for this directory are to be set in such a manner that the respective user is also owner of the directory and the sole individual that can delete files within their directory. 

<h2>Key Points Within Lab: </h2>

- <b>Creation of executable script which streamlines account username, group, and password creation.</b>
- <b>Ability of script to conduct proper error handling if a non-unique user or group name is provided.</b>
- <b>Utilization of proper syntax to allow the script to correctly and smoothly process functions and commands.</b>
- <b>Creation of a directory in the root of the file system for each new user in which the user is the owner of their directory.</b>
- <b>Utilization of the sticky bit to ensure that other user's cannot delete files in a directory that is owned by another user.</b>

<h2>Lab walk-through:</h2>

<p align="center">
In the image below, we are working within nano to create the first portion of the script which includes the set_username and set_group functions. These functions are designed to prompt for a user and group name, and after recieving input, will check /etc/passwd and /etc/group to see if those names already exist within the system. If the input names are unique, they will be accepted and a new user and group will be created. However, if the names already exist, the user will be provided with an error message and will be prompted to use a different name. <br/>
<img src="https://i.imgur.com/sjZxzd9.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
In this image we have saved the current state of the script to a file which we have called 'user_management.sh'. We have also changed the permissions of the file and made it executable so that we can proceed to run the script and ensure that it is working as intended.<br/>
<img src="https://i.imgur.com/TvZsSlz.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
In this image, we are running the script and attempting to see if the functions that we created so far are working properly. Please note that the account that I am using to create and run the script is called 'user' so it already exists in the system. Additionally, there is also a group called 'IT' that exists in the system, which I created previously for use in a separate lab. So, when the script is run and I am prompted for a username, my input of 'user' is denied and I am supplied with an error message and relevant info which shows that 'user' already exists in the system. After selecting a username that is unique, I perform the same test for the group name. As you can see, 'IT' is denied because it already exists, however, my input of 'new_group' is accepted because it is unique. So far, the script seems to be working properly, and with the addition of a few more commands, the script will be complete and fulfill all requirements of the lab. <br/>
<img src="https://i.imgur.com/1sVuzFp.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
In this image, we are back working within the script. I have added in several more commands in order to finish the script and satisfy the full requirements set forth by the lab. Some of the commands which I've added in include the useradd, groupadd, and passwd commands. The addition of these commands allow for the input user and group names to be officially added into the system once they are accepted by the script. The user will be provided with messages that state that the user and group names were successfully added, and the user will also be provided with a prompt that allows them to set a password for their account. The final few commands which follow include the mkdir, chown, and chmod commands. At this point, these commands are creating a directory at the root of the filesystem for each user, placing ownership of that directory in possession of the user that was created, and setting permissions of that directory so that the owner has full read, write, and execute permissions. Additionally, we are also utilizing the chmod command to set the sticky bit on the new user directory that was created. This makes it so only the user who is the owner of that directory is able to delete files within the directory.  <br/>
<img src="https://i.imgur.com/58AuDfn.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
In this image, we are attempting to run the script in its final form. By using the script, I am easily able to add 'test_user' who belongs to 'test_group' to the system, I am also able to give them a preliminary password, and the script also provides the new user with their own directory in which they have full control of their own files. A success message appears on the screen to showcase that all parts of the script ran accordingly,and by checking the /etc/passwd and /etc/group directories, we are able to confirm the existence of 'test_user' and 'test_group', thus confirming the success of the script.  <br/>
<img src="https://i.imgur.com/Q8roGE7.png" height="80%" width="80%" alt="AD Home Lab"/>
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
