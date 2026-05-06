## System Monitor 

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
Set cron jobs to :
- monitor disk usage 
- monitor memory 
- monitor uptime 

# Backups
Created backup archives in archives/ for logs/ in order to keep a backup of the logs. 

# Permissions
Locked down permissions to only allow the owner to have access to such information about the system.


