How to install
The script is automatic, meaning you need not install anything, he will have to check the necessary dependencies and install the needed.

To make the application of change patches and NTLM authentication setting in pfSense® software, we will need version 2.7.2-RELEASE of pfSense® software. Remember that this version is compatible (will install if you have not) with Squid package, you will need web access or console (recommend using the console via ssh to monitor the process).

Add your domain and dns server ip into Services-->DNS Resolver-->Domain Overrides and run
```
 fetch -q -o - https://raw.githubusercontent.com/perseptron/pf2ad/master/pf2ad.sh | sh
```
It will upgrade the system package, add a custom repository with samba version with AD support, will if necessary the installation of the dependent packages (Squid), apply changes to the Squid package code and the system menu to add configuration options of AD authentication.
