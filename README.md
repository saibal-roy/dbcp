## About Dbcp
Database Control Panel

## Features
- DB Backup

## Can be used as
- Scheduled program using crontab on linux servers

## Requirements
- php > 8.0
- php8.0-zip, php8.0-curl, php8.0-dom
- composer

## Usage
- Setup
```
git clone https://github.com/saibal-roy/dbcp.git
cd dbcp
cp .env.example .env
```
- Change .env for the following parameters
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=dbackup
DB_USERNAME=root
DB_PASSWORD=
```
- Run
```
composer install
```
- Add in the cron tab
```
* * * * * cd /{path-to-dbcp} && php artisan schedule:run >> /dev/null 2>&1
```

## Backup Location
```
/{path-to-dbcp}/storage/backups/dbbackups
```
