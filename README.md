<h1>Challenge Lab B: Bash Scripting</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
** This lab reflects Challenge Lab B in the 'Linux Essentials' course from the Network Development Group. **

The purpose of this lab is to demonstrate proficiency of using the built-in text editors of Linux to write a bash script which makes the user account creation process more efficient. The scenario provided within this lab states that it can be tedious, time-consuming, and leaves room for potential errors when issuing commands one-by-one in order to add a new user to the system. So, we are tasked with streamlining this process and also expected to meet the following requirements:
- The script must only accept input that allows for the creation of a unique user and group. If a user or group name already exists in the system, it must provide an 'error' message and prompt for a different user or group name. The script must also allow for a password to be set for each user created.
- The script must create a directory at the root of the filesystem which matches the name of the user that was created. The permissions for this directory are to be set in such a manner that the respective user is also owner of the directory and the sole individual that can delete files within their directory. 

<h2>Key Points Within Lab: </h2>

- <b>Creation of executable script which streamlines account username, group, and password creation.</b>
- <b>Ability of script to conduct proper error handling if a non-unique user or group name is provided.</b>
- <b>Utilization of proper syntax to allow the script to correctly and smoothly process functions and commands.</b>
- <b>Creation of a directory in the root of the file system for each new user in which the user is the owner of their directory.</b>

<h2>Lab walk-through:</h2>

<p align="center">
Pictured below..... . <br/>
<img src="https://i.imgur.com/sjZxzd9.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
Viewing the dashboard of AD server manager and all configured services on the domain controller:  <br/>
<img src="https://i.imgur.com/TvZsSlz.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
DHCP enabled but still needs configuring: <br/>
<img src="https://i.imgur.com/1sVuzFp.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
DHCP configured with scope 172.16.0.100-200:  <br/>
<img src="https://i.imgur.com/58AuDfn.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
The powershell user creation script used to create 1k+ accounts:  <br/>
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
