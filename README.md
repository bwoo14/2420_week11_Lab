# 2420_week11_Lab: Backup Service and Weather Service
By Brandon Woo and Frank Zhu


## Testing if backup server is accessible with `rsync`
- Run the command `rsync -aPv -e "ssh -i <path to ssh key>" <user>@<ip-address>:<destination>`
  <path to ssh key> = the location of the ssh key to your backup server
  <user> = the name of the user of the backup directory
  <ip-address> = the ip-address of the backup server
  <destination> = the location on the backup server you want to save the backup file

1. Run the command `vim backup-script` in your home directory

