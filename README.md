zabbix-eureka
=================

This project enhances zabbix with a externalscript which provides the following functionality:

- monitor the general health of eureka
- discover eureka applications
  (except they contain the string "TESTING" or "INTEGRATION")
- monitor disovered eureka applications

A documentation of the monitoring capabilities can be reviewed by this [html-documentation](http://htmlpreview.github.io/?https://github.com/vico-research-and-consulting/zabbix-eureka/blob/master/templates/documentation/custom__app__eureka.xml).


Usage
=====

- Define the following setting in your zabbix-server/proxy
  ```
  ExternalScripts=/etc/zabbix/externalscripts
  ```
- Add the python scripts to that folder and make them readable for the zabbix server
  ```
  cp eureka /etc/zabbix/externalscripts
  chmod 755 /etc/zabbix/externalscripts/eurekeureka
  ```
- import the template in the "templates" folder
- define a host and the ```{$EUREKA_PORT}``` marco to it
- assign the template to that host


Authors
=======

- Marc Schoechlin <marc.schoechlin@vico-research.com>

Licence
=======

see "[LICENSE](./LICENSE)" file
