Zero Downtime Migration Software Uninstallation
1. Connect as user with which you want to install the ZDM software on the Linux host
2. Stop the Zero Downtime Migration service
        $ /u01/app/zdmhome/bin/zdmservice stop
3. Run the following command to uninstall the software.
        $ /u01/app/zdmhome/bin/zdmservice stop deinstall

Example :

# Find zdmservice using locate command in linux

[zdmuser@servername ~]$ locate zdmservice 
/u01/app/zdmhome/bin/zdmservice

# Stop zdmservice

[zdmuser@servername ~]$ /u01/app/zdmhome/bin/zdmservice stop
spawn /u01/app/zdmhome/mysql/server/bin/mysqladmin --defaults-file=/u01/app/zdmbase/crsdata/servername/rhp/conf/my.cnf -u root -p shutdown
 WARNING: oracle.jwc.jmx does not exist in the configuration file. It will be TRUE by default.
[jwcctl debug] Environment ready to start JWC
[jwcctl debug] Return code of initialization: [0]

[jwcctl debug] ... BEGIN_DEBUG [Action= stop] ...
Stop JWC
[jwcctl debug] Get JWC PIDs
[jwcctl debug] Done Getting JWC PIDs
[jwcctl debug] ... JWC Container (pid=128735) ...
[jwcctl debug]     Stop command:-Dcatalina.base=/u01/app/zdmbase/crsdata/servername/rhp -Doracle.tls.enabled=false -Doracle.wlm.dbwlmlogger.logging.level=FINEST -Doracle.jwc.client.logger.file.name=/u01/app/zdmbase/crsdata/servername/rhp/logs/jwc_shutter_stdout_err_%g.log -Doracle.jwc.client.logger.file.number=10 -Doracle.jwc.client.logger.file.size=1048576 -Doracle.jwc.wallet.path=/u01/app/zdmbase/crsdata/servername/security -Doracle.jmx.login.credstore=WALLET -classpath /u01/app/zdmhome/jlib/jwc-logging.jar:/u01/app/zdmhome/jlib/jwc-client.jar:/u01/app/zdmhome/jlib/jwc-security.jar:/u01/app/zdmhome/jdk/lib/tools.jar:/u01/app/zdmhome/tomcat/lib/tomcat-juli.jar oracle.cluster.jwc.tomcat.client.ShutdownContainer 128735
[jwcctl debug] Get JWC shutter PIDs
[jwcctl debug] Done getting JWC shutter PIDs
[jwcctl debug] ... JWC shutter command (pid=251033) ...
[jwcctl debug] ... Initial Check - JWC Shutter JVM waiting (pid=251033) ...
[jwcctl debug] ... Sleep for 1 seconds ...
[jwcctl debug] ... Iteration 0 Check for JWC Shutter ...
[jwcctl debug] Get JWC shutter PIDs
[jwcctl debug] Done getting JWC shutter PIDs
[jwcctl debug] ... JWC shutter command not found ...
[jwcctl debug] ... Iteration 0 Check for JWC Container ...
[jwcctl debug] Get JWC PIDs
[jwcctl debug] Done Getting JWC PIDs
[jwcctl debug] ... JWC containers not found ...
[jwcctl debug] ... JWC Container is stopped ...
[jwcctl debug] ... STOP - Return code = 0 ...
[jwcctl debug]  ... END_DEBUG [Action=stop] ...
[jwcctl debug] Return code of AGENT: [0]

Return code is 0
zdmservice stopped successfully.

# Deinstall ZDM Software

[zdmuser@servername ~]$ /u01/app/zdmhome/bin/zdmservice stop deinstall
---------------------------------------
Running deinstall steps ...
---------------------------------------
DB_TYPE is: MYSQL
update is: 
cleanup is: 0
Confirm you want to deinstall [y/N]: y
Executing detachHome...
Starting Oracle Universal Installer...

Checking swap space: must be greater than 500 MB.   Actual 16139 MB    Passed
The inventory pointer is located at /u01/app/zdmhome/oraInst.loc
You can find the log of this install session at:
 /u01/app/zdmhome/inventory/logs/DetachHome2025-01-28_01-11-03AM.log
'DetachHome' was successful.
Deleting oracle base folder
Deleting oracle home folder
Deinstall finished successfully

Reference : 	[ZDM]: How To Install And Uninstall Zero Downtime Migration (ZDM) Software (Doc ID 2630479.1)
URL       :   https://support.oracle.com/epmos/faces/DocumentDisplay?_afrLoop=174163713347905&parent=EXTERNAL_SEARCH&sourceId=BULLETIN&id=2630479.1&_afrWindowMode=0&_adf.ctrl-state=hsepr28ce_4
              

