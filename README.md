<p align="center">
<img src="https://cdn.ttgtmedia.com/rms/onlineimages/johntheripper-figure2-f_mobile.jpg" />
</p>

<h1>John the Ripper: Analyzing the Decrypted file</h1>

In this exercise, I will analyze the file decrypted by John the Ripper and eventually get the usernames and passwords. 

<h2>Objectives</h2>

-  Learning John the Ripper essential commands.
-  Exploring vraious kali linux commands.
-  Learning more about John the Ripper. 

<h2>Environments and Technologies Used</h2>

- Virtual Machine
- Kali Linux VM
- VMWare Workstation
- John the Ripper

<h2>Operating Systems Used</h2>

- Linux

<h2>List of Prerequisites</h2>

- You need to download VMWare Workstation and have a computer of at least 8GB of RAM. Also download Kali Linux VM 

<h2>Projects steps</h2>

-  Steps : Analyzing our decrypted file

By default, “John the Ripper” will place the cracked accounts in the ~/.john directory. Since we ran this as “root”, we will find the files in /root/.john . From the root login shell, <b>cd /root/.john</b> and then <b>ls -al</b> .

.![image](https://github.com/danielbangm/Analyst-of-decripted-file/assets/22795502/c361a1a4-fe9d-42d3-9e61-89665583dd95).

Notice above, we have 3 files. Do a cat on the 3 files and let's find out what each file contains. john.log contains the accounts that were cracked
![image](https://github.com/danielbangm/Analyst-of-decripted-file/assets/22795502/f3f15898-9919-4dad-8cf9-3e169bb31ad2)

The file john.pot contains the cracked hash values
![image](https://github.com/danielbangm/Analyst-of-decripted-file/assets/22795502/c3f11ba7-1937-4f53-ab4d-981d15383cb9)

Next, let’s use the “show” command with “John the Ripper”. In a “root” shell, type in the following: <b>cd /home/kali/Downloads</b> then <b>john –show mypasswd.txt</b>
![image](https://github.com/danielbangm/Analyst-of-decripted-file/assets/22795502/03384a35-0917-47af-8979-e3c4f2a95355)

Notice that the output shows cracked passwords, their usernames followed by a passwords

- Conclusion

Applying best practices to avoid getting cracked by John the Ripper is essential to maintain robust security and protect sensitive information. Strong, unique passwords, regularly updated and not reused across different platforms, reduce the likelihood of successful brute force or dictionary attacks. Implementing multi-factor authentication adds an extra layer of security beyond passwords. Regularly auditing and updating password policies ensure they comply with the latest security standards. By doing so, organizations can significantly mitigate the risk of unauthorized access, data breaches, and potential exploitation by malicious actors using tools like John the Ripper.






