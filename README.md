# mariadb-backup.sh
a simple script to dump and rotate MariaDB backups

## Command line options
Following options are available:

| option | default | description |
| ------ | ------- | ----------- |
| v      | false   | verbose output |
| k      | 7       | number of old backups to keep |
| h      | sha265  | crypto hash to use for checksums |
| t      | /srv/backups/mariadb | root directory for all backups |
| c      | ./.my.cnf | default location of .my.cnf for user and password configuration |
| b      |         | Path to mariadb bin folder. Use this if mysqldump and mysqlshow is not in your path configuration. For example when using it in a crontab job. |
| d      |         | Database names to backup. Useful if you only want to backup some specific databases or your server has not installed mysqlshow. To pass multiple databases use a comma (,) as a separator. |