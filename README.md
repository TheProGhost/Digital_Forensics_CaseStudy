<div align="center">
<img src="./images/mv.png" alt="Logo" height=300px width=352px>
<h1>Digital Forensics </h1>
</div>

### We are doing the forensic analysis of the Hacking case from the CFReDS (Computer Forensic Reference Data Sets).

**Link: https://cfreds-archive.nist.gov/Hacking_Case.html**

* **We will be using the tool name Autopsy.**

<div>
<img src="/images/index.png" alt="Autopsy Logo">
</div>

## Scenario
>On 09/20/04 , a Dell CPi notebook computer, serial # VLQLW, was found abandoned along with a wireless PCMCIA card and an external homemade 802.11b antennae. It is suspected that this computer was used for hacking purposes, although cannot be tied to a hacking suspect, G=r=e=g S=c=h=a=r=d=t. (The equal signs are just to prevent web crawlers from indexing this name; there are no equal signs in the image files.)

>Schardt also goes by the online nickname of “Mr. Evil” and some of his associates have said that he would park his vehicle within range of Wireless Access Points (like Starbucks and other T-Mobile Hotspots) where he would then intercept internet traffic, attempting to get credit card numbers, usernames & passwords.

>Find any hacking software, evidence of their use, and any data that might have been generated. Attempt to tie the computer to the suspect, G=r=e=g S=c=h=a=r=d=t.

### Questions
1. What is the image hash? Does the acquisition and verification hash match?<br/>
```
Ans. MD5 Hash : aee4fcd9301c03b3b054623ca261959a
```

2. What operating system was used on the computer?<br/>
```
Ans. Microsoft Windows XP 
```

3. When was the install date?<br/>
```
Ans. Friday, August 20, 2004 4:18:27 AM GMT+05:30
```

4. What is the timezone settings?<br/>
```
Ans. Central Standerd Time
```

5. Who is the registered owner?<br/>
```
Ans. Registered Owner is Greg Schardt.
```

6. What is the computer account name?<br/>
```
Ans. DefaultUserName Mr. Evil
```

7. What is the primary domain name?<br/>
```
Ans. DefaultDomainName N-1A9ODN6ZXK4LQ
```

8. When was the last recorded computer shutdown date/time?<br/>
```
Ans. 2004-08-27 21:16:33.1092164 GMT+05:30
     NOTE:- We also found this by following below path “C:\WINDOWS\system32\config\software\Microsoft\WindowNT\CurrentVersion\Prefetcher\ExitTime”
```

9. How many accounts are recorded (total number)?<br/>
```
Ans. 5 ( Administrator, Guest, HelpAssistant, Mr. Evil, Support_388945a0 )
```

10. What is the account name of the user who mostly uses the computer?<br/>
```
Ans. Mr. Evil ( count 15 times)
```

11. Who was the last user to logon to the computer?<br/>
```
Ans. Mr. Evil 
     NOTE:- Can be found from path "C:\WINDOWS\system32\config\software\Microsoft\WindowNT\CurrentVersion\Winlogon"
```

12. A search for the name of “G=r=e=g S=c=h=a=r=d=t” reveals multiple hits. One of these proves that G=r=e=g S=c=h=a=r=d=t is Mr. Evil and is also the administrator of this computer. What file is it? What software program does this file relate to?<br/>
```
Ans. The perticular file which gives info is "C:\Program Files\Look@LAN\irunin.ini" and name of program is Look@LAN.
```

13.  List the network cards used by this computer<br/>
```
Ans. There are 2 Network Cards:
     First is Compaq WL110 Wireless LAN PC Card
     Second is Xircom CardBus Ethernet 100 + Modem 56 (Ethernet Interface)
     NOTE:- To find the network card the path is "C:\windows\system32\config\software\Microsoft\Windows NT\CurrentVersion\NetworkCards" 
```

14. This same file reports the IP address and MAC address of the computer. What are they?<br/>
```
Ans. File is "C:\Program Files\Look@LAN\irunin.ini".
     IP Address  : 192.168.1.111
     MAC Address : 00:10:a4:93:3e:09
```

15. An internet search for vendor name/model of NIC cards by MAC address can be used to find out which network interface was used. In the above answer, the first 3 hex characters of the MAC address report the vendor of the card. Which NIC card was used during the installation and set-up for LOOK@LAN?<br/>
```
Ans. Upon looking on MAC Lookup the company name found was: XIRCOM.
     So, the NIC card used for setup the Look@LAN is: Xircom CardBus Ethernet 100 + Modem 56 (Ethernet Interface)
```

16. Find 6 installed programs that may be used for hacking.<br/>
**Ans.** 
     <div align=center>
     <table>
          <tr>
               <th>Program Found</th>
               <th>Usage</th>
          </tr>
          <tr>
               <td>Cain & Abel v2.5 beta45</td> 
               <td>Password cracking tool</td>
          </tr>
          <tr>
               <td>Ethereal 0.10.6 v.0.10.6</td>
               <td>Advanced Network Analysis Software</td>
          </tr>
          <tr>
               <td>Network Stumbler 0.4.0 (remove only)</td> 
               <td>Wireless LAN detaction and attack</td>
          </tr>
          <tr>
               <td>Look@LAN 2.50 Build 29</td> 
               <td>an advanced network monito</td>
          </tr>
          <tr>
               <td>123 Write All Stored Password</td>
               <td>display all passwords of the currently logged on user that are stored in the Microsoft PWL file</td>
          </tr>
          <tr>
               <td>Anonymizer Bar 2.0 (remove only)</td> 
               <td>a tool that attempts to make activity on the Internet untraceable</td>
          </tr>
     </table>
     </div>

17. What is the SMTP email address for Mr. Evil?<br/>
```
Ans. E-mail Address of Mr. Evil is : whoknowsme@sbcglobal.net
     TO find this do the keyword search of SMTP.
     Then search for the file NTUSER.DAT, click on it and in the lower pane click on Text Tab. You will find it there.
```
<p align=center>
<img src="./images/Que 17.png" alt="Que17 Image">
</p>

18. What are the NNTP (news server) settings for Mr. Evil?<br/>
```
Ans. NNTP (news server) is : news.dallas.sbcglobal.net
     NNTP user name : whoknowsme@sbcglobal.net
     There is also some other info about it.
     TO find this do the keyword search of NNTP.
     Then search for the file NTUSER.DAT, click on it and in the lower pane click on Text Tab. You will find it there.
```
<p align=center>
<img src="./images/Que 18.png" alt="Que18 Image">
</p>

19. What two installed programs show this information?<br/>
```
Ans. The program show this information is MS Outlook Express.
     This thing can be varified by checking the file on given path.
     Path: "C:\Document and Settings\Mr. Evil\NTUSER.dat\Software\Microsoft\Windows\CurrentVersion\UnreadMail\whoknowsme@sbcglobal.net"
     Where it is showing the application msimn which is the exe of outlook express.
```
<p align=center>
<img src="./images/Que 19.png" alt="Que19 Image">
</p>

20. List 5 newsgroups that Mr. Evil has subscribed to?<br/>
```
Ans. The answer is in given image. 
     Note:- The newsgroups can be found at the Path: C:\Document and Settings\Mr. Evil\Local Settings\Application Data\Identities\
     {EF086998–1115–4ECD-9B13 9ADC067B4929} \Microsoft\Outlook Express
```
<div align=center>
<img src="/images/Que 20.png" alt="Que20 Image">
</div>

21. A popular IRC (Internet Relay Chat) program called MIRC was installed.  What are the user settings that was shown when the user was online and in a chat channel?<br/>
```
Ans. User  = Mini Me
     Email = none@of.ya
     nick  = Mr
     anick = mrevilrulez
     host  = Undernet: US, CA, LosAngelesSERVER:losangeles.ca.us.undernet.org:6660GROUP:Undernet

     Note:- Can be found at Path: C:\Program Files\mIRC\mirc.ini
```
<div>
<h5>Files in C:\Program Files\mIRC </h5>
<img src="./images/Que 21_1.png" alt="Que21 image1">
<h5>Content of the mirc.ini file</h5>
<img src="./images/Que 21_2.png" alt="Que21 image2">
</div>

22. This IRC program has the capability to log chat sessions. List 3 IRC channels that the user of this computer accessed.<br/>
```
Ans. To view the logs, we have to go inside the logs directory of mIRC. The channels that the user has accessed is given in below picture.
     Note:- Path is: C:\Program Files\mIRC\logs
```
<div>
<img src="./images/Que 22.png" alt="Que22 image">
</div>

23. Ethereal, a popular “sniffing” program that can be used to intercept wired and wireless internet packets was also found to be installed. When TCP packets are collected and re-assembled, the default save directory is that users \My Documents directory. What is the name of the file that contains the intercepted data?<br/>
```
Ans. To find the file, we can look to the application data of the Ethereal. The file name is "recent".
     Upon looking we can see that the recent capture is "interception".
     recent.capture_file: C:\Documents and Settings\Mr. Evil\interception

     Note:- The path to find the file is : C:\Documents and Settings\Mr. Evil\Application Data\Ethereal\recent
```
<div>
<img src="./images/Que 23.png" alt="Que23 image">
</div>

24. Viewing the file in a text format reveals much information about who and what was intercepted. What type of wireless computer was the victim (person who had his internet surfing recorded) using?<br/>
```
Ans. To get this data we have look into the file which contains intercepted data which is at 
     "C:\Documents and Settings\Mr. Evil\interception".
     The wireless computer used by the victim is: Windows CE (Pocket PC) - Version 4.20
```
<div>
<img src="./images/Que 24.png" alt="Que24 image">
</div>

25. What websites was the victim accessing?<br/>
```
Ans. Upon checking the file "interception", the website accessed by user is : 
     mobile.msn.com, MSN Hotmail Email
```
<div>
<h5>mobile.msn.com</h5>
<img src="./images/Que 25.png" alt="Que25 image">
<h5>MSN Hotmail</h5>
<img src="./images/Que 25_1.png" alt="Que25_1 image">
</div>

26. Search for the main users web based email address. What is it?<br/>
```
Ans. For this, I search in the Web History which is present in Extracted Content. 
     After searching through all the files, I found a file in which I found that 
     the user has a login to some FTP service using his email id.
     Yahoo! Mail - mrevilrulez@yahoo.com
```
<div>
<img src="./images/Que 26.png" alt="Que26 Image">
</div>

27. Yahoo mail, a popular web based email service, saves copies of the email under what file name?<br/>
```
Ans. To find the file name, I did the keyword search.
     The file found is : ShowLetter[1].htm
```
<div>
<img src="./images/Que 27.png" alt="Que27 Image">
</div>

28. How many executable files are in the recycle bin?<br/>
```
Ans. To find the files, we have to look into folder of Recycle Bin.3
     Note:- The Path is: "C:\RECYCLER\S-1–5–21–2000478354–688789844–1708537768–1003\"
```
<div>
<img src="./images/Que 28.png" alt="Que28 Images">
</div>

29. Are these files really deleted?<br/>
```
Ans. By looking at Deleted Files in the left pane, the total count of deleted files is: 1371
```
<div>
<img src="./images/Que 29.png" alt="Que29 Image">
</div>

30. How many files are actually reported to be deleted by the file system?<br/>
```
Ans. By looking at Deleted Files in the left pane, the files actually reported to be deleted by file system is: 365
```
<div>
<img src="./images/Que 30.png" alt="Que30 Image">
</div>

31. Perform a Anti-Virus check. Are there any viruses on the computer?<br/>
```
Ans. Autopsy itself performs an antivirus check & it shows its result inside Interesting Items (left-side tree structure).
     Upon looking at, we find out that there is a zip bomb.
     Location of zip bomb: C:\My Documents\FOOTPRINTING\UNIX\unix_hack.tgz
```
<div>
<img src="./images/Que 31.png" alt="Que31 Image">
</div>