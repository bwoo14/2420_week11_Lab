# 2420_week11_Lab: Backup Service and Weather Service
By Brandon Woo and Frank Zhu


## Testing if backup server is accessible with `rsync`
- Run the command `rsync -aPv -e "ssh -i <path to ssh key>" <file(s)> <user>@<ip-address>:<destination>`
  <br>\<path to ssh key\> = the location of the ssh key to your backup server
  <br>\<file(s)\> = the name of the file and the 
  <br>\<user\> = the name of the user of the backup directory
  <br>\<ip-address\> = the ip-address of the backup server
  <br>\<destination\> = the location on the backup server you want to save the backup file
  ![](images/test_rsync.png)
<br>1. Run the command `vim backup-script` in your home directory
  <br>write shebang at the top then paste in rsync command that you ran it should look like this
  ![](images/trsync.png)
  <br>- save and exit out of file and then run `chmod u+x backup-script`
  <br>Remove the copied directory from your backup server
  <br>Run your backup script with `./backup-script`
  ![](images/rsyscrt.png)
  


