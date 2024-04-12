Ubuntu (but not all Linux distros) have some preconfigured folders that you can drop your file in
* /etc/cron.daily
* /etc/cron.hourly
* /etc/cron.monthly
* /etc/cron.weekly

This will run your files on time cadence specified in the folder name

Launch a crontab in an editor of your choice
```
crontab -e
```

Here is an example cronjob
NOTE: Make sure your file has execute permissions first (run either chmod 700 or chmod +x [filename])
```
* * * * * /home/ubuntu/my_bin/make_new_file

```
