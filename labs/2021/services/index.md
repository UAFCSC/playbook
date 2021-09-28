# Securing Services
Presented September 23, 2021

## Lab Procedure
Each lab VM is configured with various insecure services, as well as a check command to check if certain severe
vulnerabilities are still present. To begin, log into your assigned VM. Run the check command, `lab_check`, to get a
list of issues that need to be resolved. Run this command to check your progress. `lab_check` will confirm when all
checks are passing.

## Resources
Various resources are listed below, though many more exist and may be found through web searches easily.

### Apache2
Apache2's documentation can be found at [http://httpd.apache.org/docs/2.4/](http://httpd.apache.org/docs/2.4/). There is
also a [directive quick reference](https://httpd.apache.org/docs/2.4/mod/quickreference.html). Particularly relevant to
this lab is the [`Directory` directive](https://httpd.apache.org/docs/2.4/mod/core.html#directory).

For this particular lab, the relevant configuration file will be present at
`/etc/apache2/sites-enabled/000-default.conf`.

### FTP (vsftpd)
Useful documentation for `vsftpd` can be found on Ubuntu's Community Help Wiki:
[https://help.ubuntu.com/community/vsftpd](https://help.ubuntu.com/community/vsftpd). `vsftpd`'s configuration file is
located at `/etc/vsftpd.conf`.

### MariaDB
Information on securing MariaDB can be found in their knowledge base:
[https://mariadb.com/kb/en/securing-mariadb/](https://mariadb.com/kb/en/securing-mariadb/).

### SSH
Information on OpenSSH Server's configuration file can be found here:
[https://www.ssh.com/academy/ssh/sshd_config](https://www.ssh.com/academy/ssh/sshd_config). The configuration file
itself is in `/etc/ssh/sshd_config`.

## Lab Setup
### CSC vSphere
The template for this lab is available on our vSphere instance.

### Manual Setup
All of the required scripts can be found here:
[https://gist.github.com/katlyn/21bcf3d68bb52e03abf598f4db697e74](https://gist.github.com/katlyn/21bcf3d68bb52e03abf598f4db697e74).
You are able to use `git` to clone all required files with the link provided on the gist's page. Running `bash setup.sh` will install all required dependencies, implement insecure services, and compile and install the check script.
`setup.sh` expects an Ubuntu-based system to be used. **Using this script *will* make the machine it is run on
insecure.** Do not use it unless you are on a VM or otherwise prepared for the consequences.
