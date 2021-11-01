# LinuxSplunkInstall
root@UbuntuDesktop:/tmp# wget -O splunk-8.2.3-cd0848707637-Linux-x86_64.tgz 'https://download.splunk.com/products/splunk/releases/8.2.3/linux/splunk-8.2.3-cd0848707637-Linux-x86_64.tgz'
--2021-11-01 17:25:52--  https://download.splunk.com/products/splunk/releases/8.2.3/linux/splunk-8.2.3-cd0848707637-Linux-x86_64.tgz
Resolving download.splunk.com (download.splunk.com)... 52.84.121.123, 52.84.121.118, 52.84.121.15, ...
Connecting to download.splunk.com (download.splunk.com)|52.84.121.123|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 569235098 (543M) [binary/octet-stream]
Saving to: ‘splunk-8.2.3-cd0848707637-Linux-x86_64.tgz’

splunk-8.2.3-c 100% 542.86M  23.5MB/s    in 22s           

2021-11-01 17:26:14 (24.8 MB/s) - ‘splunk-8.2.3-cd0848707637-Linux-x86_64.tgz’ saved [569235098/569235098]

You have new mail in /var/mail/root
root@UbuntuDesktop:/tmp# cd
root@UbuntuDesktop:~# cd /opt
root@UbuntuDesktop:/opt# cd
You have new mail in /var/mail/root
root@UbuntuDesktop:~# ls
root@UbuntuDesktop:~# ls
root@UbuntuDesktop:~# cd
root@UbuntuDesktop:~# ls
root@UbuntuDesktop:~# cd /opt
root@UbuntuDesktop:/opt# ls
chkrootkit  logrotate                 wildpwn
containerd  VBoxGuestAdditions-6.1.6
root@UbuntuDesktop:/opt# tar -zxf /tmp/splunk^C
root@UbuntuDesktop:/opt# tar -zxf /tmp/splunk-8.2.3-cd0848707637-Linux-x86_64.tgz
You have new mail in /var/mail/root
root@UbuntuDesktop:/opt# ls
chkrootkit  logrotate  VBoxGuestAdditions-6.1.6
containerd  splunk     wildpwn
root@UbuntuDesktop:/opt# cd
You have new mail in /var/mail/root
root@UbuntuDesktop:~# /opt/splunk# /opt/splunk/bin/splunk start --accept-license
bash: /opt/splunk#: No such file or directory
root@UbuntuDesktop:~# /opt/splunk
bash: /opt/splunk: Is a directory
root@UbuntuDesktop:~# cd opt
bash: cd: opt: No such file or directory
root@UbuntuDesktop:~# /opt/
bash: /opt/: Is a directory
root@UbuntuDesktop:~# /opt/splunk/bin/splunk start --accept-license

This appears to be your first time running this version of Splunk.

Splunk software must create an administrator account during startup. Otherwise, you cannot log in.
Create credentials for the administrator account.
Characters do not appear on the screen when you type in credentials.

Please enter an administrator username: bmalin
Password must contain at least:
   * 8 total printable ASCII character(s).
Please enter a new password:
Please confirm new password:
Copying '/opt/splunk/etc/openldap/ldap.conf.default' to '/opt/splunk/etc/openldap/ldap.conf'.
Generating RSA private key, 2048 bit long modulus
.....................................................................................................................................+++++
............................................................................................................................................................+++++
e is 65537 (0x10001)
writing RSA key

Generating RSA private key, 2048 bit long modulus
...................................+++++
.........+++++
e is 65537 (0x10001)
writing RSA key

Moving '/opt/splunk/share/splunk/search_mrsparkle/modules.new' to '/opt/splunk/share/splunk/search_mrsparkle/modules'.

Splunk> The IT Search Engine.

Checking prerequisites...
    Checking http port [8000]: not available
ERROR: http port [8000] - port is already bound.  Splunk needs to use this port.
Would you like to change ports? [y/n]: y
Enter a new http port: 443
Setting http to port: 443
The server's web port has been changed.
You need to restart the Splunk Web Server (splunkweb) for your changes to take effect.
    Checking http port [443]: open
    Checking mgmt port [8089]: open
    Checking appserver port [127.0.0.1:8065]: open
    Checking kvstore port [8191]: open
    Checking configuration... Done.
        Creating: /opt/splunk/var/run/splunk/appserver/i18n
        Creating: /opt/splunk/var/run/splunk/appserver/modules/static/css
        Creating: /opt/splunk/var/run/splunk/upload
        Creating: /opt/splunk/var/run/splunk/search_telemetry
        Creating: /opt/splunk/var/spool/splunk
        Creating: /opt/splunk/var/spool/dirmoncache
        Creating: /opt/splunk/var/lib/splunk/authDb
        Creating: /opt/splunk/var/lib/splunk/hashDb
New certs have been generated in '/opt/splunk/etc/auth'.
    Checking critical directories...    Done
    Checking indexes...
        Validated: _audit _internal _introspection _metrics _metrics_rollup _telemetry _thefishbucket history main summary
    Done
    Checking filesystem compatibility...  Done
    Checking conf files for problems...
    Done
    Checking default conf files for edits...
    Validating installed files against hashes from '/opt/splunk/splunk-8.2.3-cd0848707637-linux-2.6-x86_64-manifest'
    All installed files intact.
    Done
All preliminary checks passed.

Starting splunk server daemon (splunkd)...  
Generating a RSA private key
.......+++++
..........+++++
writing new private key to 'privKeySecure.pem'
-----
Signature ok
subject=/CN=UbuntuDesktop/O=SplunkUser
Getting CA Private Key
writing RSA key
Done


Waiting for web server at http://127.0.0.1:443 to be available............. Done


If you get stuck, we're here to help.  
Look for answers here: http://docs.splunk.com

The Splunk web interface is at http://UbuntuDesktop:443

You have new mail in /var/mail/root
root@UbuntuDesktop:~# 
