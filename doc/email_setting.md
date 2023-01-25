# 1. *Collect information from postmark*
![postmark.png](image%2Fpostmark.png)
https://account.postmarkapp.com/servers/10155452/streams/broadcast/settings

These information will be used later
* smtp server in `Server` field   
smtp-broadcasts.postmarkapp.com
* click `Generate an SMTP Token`   
Keep Access key as email username for later usage   
Keep Token as email password for later usage   

# 2. *Create email domain*
![emailDomain.png](image%2FemailDomain.png)
* Incoming Settings   
  See setting in picture
* Outgoing Settings     
Server: smtp-broadcasts.postmarkapp.com     
Port: 587

# 3. *Create email account*
![emailAccount.png](image%2FemailAccount.png)
* Email Address   
  It's email of sender.
* Domain    
  Use the email domain created in the previous step
* Authentication 
  Use username and password retrieved from postmark setting previously as `Alternative Email ID` and`Password` 
* enable  `Enable Outgoing`
* ` Default Outgoing`
# 4. sender set
![sender.png](image%2Fsender.png)
