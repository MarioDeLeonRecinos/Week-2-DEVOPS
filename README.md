
# Week 2 DEVOPS

Weekly challenge with the scripts made for it

## Renaming files script

To run tests, run the following command

For the first script this following command is an example for running it
with the directory line being the location of the directory to change

```bash
  ./script_1 -d directory
```

For the first script this following command is an example for running it
with the interactive mode

```bash
  ./script_1 -i
```

Or if you want to see all options for using it

```bash
  ./script_1 -h
```

## Backups script

Script for the backup of specific files saved in a txt file in the directory /tmp/backup_script2/prueba.txt

For the script the usage is the following first adding the file direction in the system with the following command

```bash
  ./script_2 -d directory
```

After the last script you will need to change the configuration file of cron with crontab adding the line after the first command and saving said file and next we verify of the correct start of the cron service and if its not running we start it

```bash
  crontab -e
  43 16 * * * /home/mario/github/Week-2-DEVOPS/script_2 > /dev/null 2>&1
  service cron status
  sudo service cron start
```

Or you can run said command directly from console with the next call from the cloned directory

```bash
  ./script_2
```

Or if you want to see all options

```bash
  ./script_2 -h
```

## NGINX Users script

Script for the creation of a user in the authentication deployed for nginx service that verifies the user and password if provided in the command call or an interactive mode

For the command call without interaction you need to use the following command changing user with your user name to be and password with the password of said user to be created

```bash
  ./script_3 -u user -p password
```

Next for the interactive mode you call it like the next line

```bash
  ./script_3 -i
```

Or if you want to see all options

```bash
  ./script_3 -h
```
