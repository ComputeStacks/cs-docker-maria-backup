# MariaDB Backup Utility

**No Longer Maintained. Current versions of ComputeStacks rely on the included mariabackup within the existing mariadb container**.

See: https://mariadb.com/kb/en/library/mariabackup-overview/ 

This image, unlike other similar container images, is designed to startup and run detached (using runinit) and have the mariadb volumes mounted to `/data`. 

When it's time to perform a backup, execute: `docker exec -i <container> mariabackup <options>`

Note: This is designed to work in conjunction with the ComputeStacks backup agent.