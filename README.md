# dar
Simple directory arbitrary rotate system

# help
Usage: `dar [-options]`<br />
where options include:
-	`-f | --classifier`		project name for exemple (will be a root directory for all your files)
-	`-r | --rotate`		rotate counter (e.g: -r=10, default: 10)
-	`-o | --output`		output directory, location where dumps will be stored (e.g: -o=/home/filestorotate)
-	`-h | --help`		shows this help

Crontab entries
- `* * * * * /usr/local/sbin/dar -r=60 -f="minutely1" -o="/home/filesbackups"`
- `*/5 * * * * /usr/local/sbin/dar -r=12 -f="minutely5" -o="/home/filesbackups"`
- `0 * * * * /usr/local/sbin/dar -r=24 -f="hourly" -o="/home/filesbackups"`
- `0 1 * * * /usr/local/sbin/dar -r=30 -f="daily" -o="/home/filesbackups"`
- `0 0 * * 0 /usr/local/sbin/dar -r=52 -f="weekly" -o="/home/filesbackups"`
- `0 0 1 * * /usr/local/sbin/dar -r=12 -f="monthly" -o="/home/filesbackups"`
