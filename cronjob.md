Ubuntu (but not all Linux distros) have some preconfigured folders that you can drop your file in
* /etc/cron.daily
* /etc/cron.hourly
* /etc/cron.monthly
* /etc/cron.weekly

This will run your files on time cadence specified in the folder name

Launch a crontab in an editor of your choice - might default to running as root
```
crontab -e
```

Or run this cmd to run the cronjob as a user other than root (Recommended)
```
crontab -u [username] -e
```

Here is an example cronjob
NOTE: Make sure your file has execute permissions first (run either chmod 700 or chmod +x [filename])
```
*/2 * * * * /home/ubuntu/my_bin/make_new_file
```

NOTE: The */2 means to run the file every two minutes

Check out crontab guru to convert the stars into the job schedule you would like your file to run:
https://crontab.guru/
