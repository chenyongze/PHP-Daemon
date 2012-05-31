# PHP-Daemon (Stephen Chen) #

Use PHP &amp; Shell to create long-runling, multi-process, multi-thread deamon. Use service to manage the daemon.

> Note: Make sure server has been installed PHP.

#### Requires: ###
* PHP
* Linux os (Based on Redhat)

* ###Directory:
	**Daemon.php**
	PHP Controller. Do not edit this file.
	**PHPDaemon**
	Sample Shell
	**Debug**
	Debug Directory
	**--PHPDaemon.php**
	Debug this file in your broswer
	**Lib**
	Library
	**--common.php**
	Share File
	**Log**
	Log Directory. Function setLog may use this Directory
	**Script**
	PHP Script
	**--PHPDaemon.php**
	This file is the main logic PHP

* ###How to:
1. Upload files.

2. Run the following scripts to modify file priviledge:

   chmod a+x PHPDaemon Daemon.php;

   set ff=unix 

3. Edit PHPDaemon. Define APP_PATH, MODULE & PROCESS.

4. Copy or link PHPDaemon to /etc/init.d/ (`chkconfig --add PHPDaemon` If wants autostart)

5. Implement PHPDaemon.php.

6. Run the following scripts to startup:

   Service PHPDaemon Start; (Start|Stop|Status)

* ###Lock File:
/var/lock/subsys/PHPDaemon.lock

* ###PID File:
/var/run/PHPDaemon.pid