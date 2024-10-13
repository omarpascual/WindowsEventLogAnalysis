# WindowsEventLogAnalysis
IR_RemoteConn_log
<br />
<br />
In this Analysis I look at a saved log name IR_RemoteConn_LOG.evtx. As I search though the log, I find event ID 1194 where user is name eviluser. We see this user attempting to create a connection. We can see their IP address as well as the date and time they attempted: 2/7/2020 11:15:59 AM
<br />

![window](https://github.com/user-attachments/assets/49da48db-88e5-4e82-acd5-39f0d0272ff9)
<br />

IR_Security_Log
<br />
<br />
While analyzing this log, Event ID 4624 shows that eviluser did connect. Meaning an account was successfull and this is an exisiting user in the system
<br />
![Window](https://github.com/user-attachments/assets/6229bf1a-105d-436f-b8c8-ce60a43fe850)
<br />
We want to find out when the user was created. I find that in Event ID 4720 was when the user was created and I filterd Current log to only see Event ID 4720
<br />
![Window](https://github.com/user-attachments/assets/5010a298-c3b2-425c-8958-e8ab085b50a0)
<br />
IR_Incident
<br />
<br />
Next i look at another log named IR_Incident where I see that a services was installed in the system
<br />
![Window](https://github.com/user-attachments/assets/eadc394f-c22e-4a0a-b542-afe17f225bd0)
<br />
<br />
Back with IR_Security_Log I filter Event ID 5379 where I see when account credentials were interacted with. We see activity from user Anthony as well as System. I then filter 4625 to see if i can find any failed logins. I see continued failed logins for user Anthony.
<br />
![Window](https://github.com/user-attachments/assets/df75a5b2-3cda-4ad2-a882-b8315279eac6)
<br />
I examine event ID 4648 and notice that credential dumping taking place.
<br />
![Window](https://github.com/user-attachments/assets/4d90a45e-bebd-4c0e-870b-573a2ea71f16)
<br/>
For reference on credential dumping ---> (https://attack.mitre.org/techniques/T1003/)
<br />
<br />
In event 4624 with different logon type, my focus is now in Logon Type 10. It suggest remote/network access. IP address of 192.168.56.102, another computer on the network.
I search for another event but with Logon Type 3 where i can get info on the workstation name. It is indeed another workstation name kali.
<br />
![Window](https://github.com/user-attachments/assets/7eb687ee-dea5-4f53-a194-91f320ded618)
<br />
![Window](https://github.com/user-attachments/assets/269e6c6a-b720-4510-b69a-7858f9f40506)
