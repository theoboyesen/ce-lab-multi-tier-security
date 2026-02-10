BASTION -> DATABASE TIER

[ec2-user@ip-172-31-69-158 ~]$ ssh -i security-lab-key.pem ec2-user@172.31.67.239
The authenticity of host '172.31.67.239 (172.31.67.239)' can't be established.
ED25519 key fingerprint is SHA256:Rruf7hZp8WXv6qQFrg4N1b6j1xJqN2D17x+rUX9hlsY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '172.31.67.239' (ED25519) to the list of known hosts.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0444 for 'security-lab-key.pem' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "security-lab-key.pem": bad permissions
ec2-user@172.31.67.239: Permission denied (publickey,gssapi-keyex,gssapi-with-mic).
[ec2-user@ip-172-31-69-158 ~]$ chmod 400 security-lab-key.pem
[ec2-user@ip-172-31-69-158 ~]$ ssh -i security-lab-key.pem ec2-user@172.31.67.239
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'


BASTION -> APP TIER

[ec2-user@ip-172-31-69-158 ~]$ ssh -i security-lab-key.pem ec2-user@172.31.73.252
The authenticity of host '172.31.73.252 (172.31.73.252)' can't be established.
ED25519 key fingerprint is SHA256:z3lfQmM8MsbrC/cScqZgsNVVsvwYbpbyjfKFCX3/0T0.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '172.31.73.252' (ED25519) to the list of known hosts.
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'


BASTION -> WEB TIER

[ec2-user@ip-172-31-69-158 ~]$ ssh -i security-lab-key.pem ec2-user@172.31.77.225
The authenticity of host '172.31.77.225 (172.31.77.225)' can't be established.
ED25519 key fingerprint is SHA256:IR7XhQtpQhg2LvctGIO1f2KDEPghzXPnsfHfwcs4XGU.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '172.31.77.225' (ED25519) to the list of known hosts.
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'

LOCAL -> DATABASE TIER

PS C:\Users\tboye\downloads> ssh -i security-lab-key.pem ec2-user@172.31.67.239
ssh: connect to host 172.31.67.239 port 22: Connection timed out

LOCAL -> APP TIER

PS C:\Users\tboye\downloads> ssh -i security-lab-key.pem ec2-user@172.31.73.252
ssh: connect to host 172.31.67.239 port 22: Connection timed out

LOCAL -> WEB TIER 

PS C:\Users\tboye\downloads> ssh -i security-lab-key.pem ec2-user@172.31.77.225
ssh: connect to host 172.31.77.225 port 22: Connection timed out
