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
