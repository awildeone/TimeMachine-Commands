# Time Machine Terminal Controls

This is a collection of commands that can be used to control Time Machine on macOS

Current List (in Progress):
 - Schedule TimeMachine interval (CronTab)

---

## Time Machine Scheduler

 1. Create tm_scheduler.sh under any directory you want to keep the file.

    `vim tm_scheduler.sh`

    Add script:
    `#!/bin/sh
    /usr/bin/tmutil startbackup`

 2. Create a crontab to run the command

    `crontab -e`
3. In the crontab editor (Default VIM), add the following template in the repo

`crontab example.txt`


4. As a new line, add your crontab command using the template as a guide. To run a shell script, you will need to add /bin/sh in the line. The following command will run at minute 0 of every hour, every day.

`0 * * * * /bin/sh /path/to/schedule.sh`

5. Exit out of Vim while saving on quit (`:wq`)
6. Check the status of the backup at the top of the hour.
