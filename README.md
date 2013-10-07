exchange-cross-forest-mover-for-mailboxes with GUI
=========================================

moves exchange mailboxes cross forest (between 2 domains)

Before you start:
- create trust between the forests
- setup MS ADMT
- move the user to the new domain (transfer the SID to new Users in the new domain)
- 



This script does the following:

Linked Mailbox:
http://www.msxfaq.de/migration/linkedmailbox.htm

Prepare Move Request:
http://www.msxfaq.de/migration/preparemoverequest.htm

Prepare Mailboxes for Cross-Forest Moves Using the Prepare-MoveRequest.ps1 script in the Shell:
http://technet.microsoft.com/en-us/library/ee861103.aspx

Create a Remote Move Request That has Exchange 2010 in Both Forests
http://technet.microsoft.com/en-us/library/dd351280.aspx

Create a Remote Legacy Move Request Where One of the Forests Doesn't Have Exchange 2010:
http://technet.microsoft.com/en-us/library/dd876952.aspx

Prepare Mailboxes for Cross-Forest Move Requests:
http://technet.microsoft.com/en-us/library/ee633491.aspx

run this on the old Exchange (2003?):
csvde -l displayName,samAccountName,mailNickname,mail,targetAddress,proxyAddresses,altRecipient -r "objectclass=user" -f c:\transfer_Mailboxes_to_exchange_2010.csv

On the new Exchange you can run the ps1 script attached to this repository.


