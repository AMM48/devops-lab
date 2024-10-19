# Log Archive Tool
A Bash script to archive logs from a specified directory, with options to store them locally, upload to an S3 bucket, and schedule as a cron job.

## Getting Started
1. **Clone the repository**
    ```
    git clone https://github.com/AMM48/devops-lab.git
    cd log-archive-tool
    ```

2. **Make the script executable**
    ```
    chmod +x log-archive
    mv log-archive /usr/local/bin/
    ```
3. **Execute the script**
    ```
    log-archive
    ```

## Usage
```
log-archive -l <log-directory> -a <archive-directory> [-s <S3-URI>] [-d] [-t]
```

### Required:
- `-l <log-directory>`  
  Directory containing logs to archive (e.g. `/var/log/logs-dir`)

- `-a <archive-directory>`  
  Local directory where archived logs will be stored (e.g. `/var/log/compressed`)

### Optional:
- `-s <S3-URI>`  
  S3 URI to store archived logs on an S3 bucket (e.g. `s3://amzn-s3-logs-bucket`)

- `-d`  
  Delete original log files after they have been archived.

- `-t`  
  Schedule the script as a cron job.

<br/>

This project is part of [roadmap.sh](https://roadmap.sh/projects/log-archive-tool) DevOps projects.