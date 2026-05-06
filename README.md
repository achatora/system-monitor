# System Monitor 

# Overview 
Automated Linux system health monitor that logs disk usage, memory and uptime on a scheduled basis using cron, with archived log management and hardened file permissions.

# Structure 
/home/siralfredthegreat/system-monitor/
├── archives
│   ├── disk_log_backup.tar.gz
│   ├── memory_log_backup.tar.gz
│   └── system_log_backup.tar.gz
├── cronjob_commands.txt
├── logs
│   ├── disk.log
│   ├── memory.log
│   └── system.log
├── permissions.txt
└── README.md

# Cron jobs
Scheduled the following cron jobs to automate system monitoring:

Log disk usage every hour:
0 * * * * echo "$(du -sh) - $(date)" >> /home/siralfredthegreat/system-monitor/logs/disk.log

Log memory usage every hour:
0 * * * * echo "$(free -h) - $(date)" >> /home/siralfredthegreat/system-monitor/logs/memory.log

Log date and uptime every day at 9AM:
0 9 * * * echo "$(date) - $(uptime)" >> /home/siralfredthegreat/system-monitor/logs/system.log


# Backups
Created backup archives in archives/ for logs/ in order to keep a backup of the logs. 

# Permissions
Locked down permissions to only allow the owner to have access to such information about the system.


