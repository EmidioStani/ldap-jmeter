# Description

This jmeter test case is used to test an ldap user directory perfoming the following operations:
1. Add user (with attributes cn, sn, userPassword, mail)
2. modify the user just created by changing the mail attribute
3. search the user with the modified mail attribute
4. delete the user created

The 4 operations are executed sequentially by a certain number of parallel users (threads) that can be specified as parameter. The number of times that the 4 operations are executed sequentially can be also specificed as parameter.

# Usage

The test case can be launched by GUI or by command line. By command line you can specify the following parameters:

* __ldap.server__ (default localhost)
* __ldap.port__ (default 1389)
* __ldap.base__ (default ou=users\,dc=csde\,dc=esa\,dc=int)
* __ldap.admin__ (default cn=admin)
* __ldap.pass__ (default password)
* __ldap.threads__ (default 10)
* __ldap.rampup__ (default 0)
* __ldap.loop__ (default 10)
* __ldap.report__ (default C:\TEMP\report.jtl)

An example by command line would be:


jmeter.bat -n -t opendj.jmx -Jldap.server=opendj -Jldap.pass=mypassword

