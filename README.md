# Linux-Logrotate
System Administrator - KodeKloud


#### The Nautilus DevOps team is ready to launch a new application, which they will deploy on app servers in Stratos Datacenter. They are expecting significant traffic/usage of squid on app servers after that. This will generate massive logs, creating huge log files. To utilise the storage efficiently, they need to compress the log files and need to rotate old logs. Check the requirements shared below:



#### a. In all app servers install squid package.

#### b. Using logrotate configure squid logs rotation to monthly and keep only 3 rotated logs.

 ##### (If by default log rotation is set, then please update configuration as needed)
 
 ##### Login to app server and swith to root user.
 ```
  ssh tony@stapp01
  sudo su -
  ```
  #### Here we need to install squid package and keep log rotation monthly and three times
  
  ```
  yum install squid
  ```
  #### Navigate to logrotate folder and configure squid logs monthly and keep only 3 rotated logs.
  
  ```
  cat /etc/logrotate.d/
  11 /squid/
  vi /etc/logrotate.d/squid/
  ```
  
  #### Now start and validate if squid is running or not
  ```
  systemctl start squid
   systemctl status squid
  ```
  
  #### I have done only for one app server , do this same configuration to all app servers.
