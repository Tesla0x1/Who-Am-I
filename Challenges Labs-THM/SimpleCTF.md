# Simple CTF - TryHackMe Writeup 🚩
**Platform:** [TryHackMe](https://tryhackme.com/room/easyctf)
**Difficulty:** Easy

## Answer the questions below
  **How many services are running under port 1000?** *[2]*
  
      ``` sudo nmap -sV -p 1-1001 10.112.129.59
          PORT   STATE SERVICE VERSION
          21/tcp open  ftp     vsftpd 3.0.3
          80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
          Service Info: OS: Unix ```


  **What is running on the higher port?** *[SSH]*
  
    ``` sudo nmap -sV -p- 10.112.129.59
        PORT     STATE SERVICE VERSION
        21/tcp   open  ftp     vsftpd 3.0.3
        80/tcp   open  http    Apache httpd 2.4.18 ((Ubuntu))
        2222/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
        Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel ```

  **What's the CVE you're using against the application?** *[CVE-2019–9053]*
  
     ``` Start Fuzz Dir , Found Dir name = Simple , after found the dir open site http://10.112.129.59/simple  , and see last page found version [by Made Simple Version 2.2.8]
         copy the version and search in google , what CVE "CMS 2.2.8"   
     
      ``` 

 **To what kind of vulnerability is the application vulnerable?** *[SQLI]*

 ### Now We Try Login  Way FTP :
 
    ```
      ftp 10.114.170.115
           Connected to 10.114.170.115.
           220 (vsFTPd 3.0.3)
           Name (10.114.170.115:t3sla):
           530 This FTP server is anonymous only.
           ftp: Login failed
         
       👉 Try Login with anonymous 
    ftp 10.114.170.115
           Connected to 10.114.170.115.
           220 (vsFTPd 3.0.3)
           Name (10.114.170.115:t3sla): anonymous
           230 Login successful.
           Remote system type is UNIX.
          Using binary mode to transfer files.  👉While you are trying to enter FTP, a specific file is being transferred, now how do we obtain this file 👈

      🔦 Using Wget to get data transfer 
    wget -m --no-passive   ftp://anonymous@10.114.170.115
      we see name file == ForMitch.txt  💡 Point - The data in file it is Massage Directed to a person : The Name Person🕵 mitch 
     
    ```   
            
