# Changelog

## 2.1.0

### General
- Added a variable *useCompression* to use compression (.tar.gz) for file and data directory (enabled by default, this was also the default behavior before this option was implemented). 
- You can disable compression of these directories (.tar) if you use some other (archiving) backup mechanism which utilizes the Nextcloud backup and restore scripts (e.g. Borg Backup, see here: https://codeberg.org/DecaTec/Linux-Server-Backup)

## 2.0.0

### General
- Added script (`setup.sh`) for an (more or less) automated setup of the backup and restore scripts (utilizing OCC in order to gather information about Nextcloud instance).

## 1.1.1

### Backup
- When a backup is cancelled, the webserver is restartet automatically.

## 1.1.0

### Backup
- New variable *ignoreUpdaterBackups*: When set to true, the backups of Nextcloud's updater are not included in the backups (default: *false*).

## 1.0.0

### General
- Versioning of Nextcloud-Backup-Restore.
- The database system (MySQL/MariaDB or PostgreSQL) is configured in the variable area of the scripts, so it's not necessary to comment/uncomment the specific database commands.
- Special characters for the database password can be used now.
- Single quotes for variables.

### Restore
- The commands for restoring the database are checked at the beginning of the script. Is the specific database system is not installed, the restore is cancelled.
- The default main backup directory now is the same as in the backup script.