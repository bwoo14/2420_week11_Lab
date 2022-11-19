# 2420_week11_Lab: Backup Service and Weather Service
By Brandon Woo and Frank Zhu


## Testing if backup server is accessible with `rsync`
- Run the command `rsync -aPv -e "ssh -i <path to ssh key>" <file(s)> <user>@<ip-address>:<destination>`
  <br><path to ssh key> = the location of the ssh key to your backup server
  <br><file(s)> = the name of the file and the 
  <br><user> = the name of the user of the backup directory
  <br><ip-address> = the ip-address of the backup server
  <br><destination> = the location on the backup server you want to save the backup file
  ![](images/test-rsync.png)

1. Run the command `vim backup-script` in your home directory

