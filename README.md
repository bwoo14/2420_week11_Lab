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
- Run the command `vim backup-script` in your home directory
- Write shebang at the top then paste in rsync command that you ran it should look like this
![](images/trsync.png)
- Save and exit out of file. Run `chmod u+x backup-script`
- Delete the newly copied directory from your backup server so that you can test to see if you're script works
- Run your backup script with `./backup-script` <br>
![](images/rsyscrt.png)
## Making the backup-script
- Make a configuration file in the `/etc` directory by running `sudo touch backup_script.conf`
![](images/confsspng.png)
- The new script should look like this
![](images/newscr.png)


## Writing the Service File
- Run the command `vim backup-script.service`
- Edit the file so it has the following content:
![](images/servicefile.png)

## Writing the Timer File
- Run the command `vim backup-script.timer`
- Edit the file so it has the following content:
![](images/timerfile.png)
- `RandomizedDelaySec=5m` the `5m` value can be changed to what the user requires. 
- This value will allow the script to randomize the start time of each server that requires the backup from 0 seconds to the value required by the user.
- `RandomizedDelaySec` will change the value given into seconds.

## Ensure your timezone is set to the correct timezone
- Use the command `sudo timedatectl set-timezone America/Vancouver`
- Can change `America/Vancouver` to the desired timezone
