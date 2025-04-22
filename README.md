Exp 5 : Set a Cron job 

AIM:
To set a Cron job.  

EQUIPMENTS REQUIRED:

Hardware: Minimum 4 GB RAM and 25 GB storage – essential for running services like Cockpit and handling system updates smoothly.
Software: Red Hat Enterprise Linux (RHEL) or any open-source Linux OS like Fedora or CentOS Stream – used for system administration and repository creation.

PROCEDURE & COMMENTS:

Editing crontab
 The first line [root@servera:~]# crontab -e harry edits the crontab for the user harry. The crontab command is used to manage cron jobs for users. The -e option specifies that the user's crontab file should be opened in a text editor. In this case, since the user executing the command is root (the system administrator), they are able to edit the crontab for another user (harry).
Adding a cron job 
The line 30 12 * * * /bin/bash /home/harry/backup.sh is most likely the line that was added to the crontab file. This line defines a new cron job. Cron jobs use a specific format to define the schedule and command to be executed. The format is: minute hour day of month month day of week command Each field is separated by a space and defines a specific value or range of values. An asterisk (*) in any field represents "all possible values" for that field. 
In this case, the cron job is defined as follows: 
• Minute: 30 - This means the job will run at the 30th minute of every hour. 
• Hour: 12 - This means the job will run at 12 o'clock. 
• Day of month: * - This wildcard symbol indicates that the job will run on every day of the month. 
• Month: * - This wildcard symbol indicates that the job will run in every month of the year. 
• Day of week: * - This wildcard symbol indicates that the job will run on every day of the week (Monday through Sunday). 
• Command: /bin/bash /home/harry/backup.sh - This specifies the command to be executed. The /bin/bash part tells the system to use the Bash shell to execute the script. The /home/harry/backup.sh part specifies the path to the script that will be run. 
Saving the crontab  
After editing the crontab file, the user would typically save and exit the text editor. Since we don't see the specific commands used to save the file, I can't say for sure how this was done in this instance. In summary, these commands set up a cron job to run a script named /home/harry/ backup.sh at 12:30 every day. The script itself is not shown in the image so it is impossible to know what the script does. 

EXPECTED OUTPUT

![OSOS_EXP_05](https://github.com/user-attachments/assets/3cdb97a9-9023-4ee0-86db-85ac85dd403b)

RESULT:
Thus a cron job has been set successfully for the user harry.

