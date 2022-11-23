vi /etc/postfix/main.cf
systemctl restart postfix.service 
systemctl status postfix.service 
mutt
echo "test message" | mail -s "Test email" root@localhost
mutt
vi message
mail -s "Boss email" root@localhost < message 
mutt
cat /etc/services | grep smtp
telnet localhost 25
mutt
less /var/spool/mail/root
less /var/spool/mail/student
echo "test message" | mail -s "Test email" student@localhost
less /var/spool/mail/student
vi /etc/postfix/main.cf
vi /etc/postfix/sasl_passwd
chmod 0600 /etc/postfix/sasl_passwd
postmap /etc/postfix/sasl_passwd
postfix check 
systemctl restart postfix.service 
systemctl status postfix.service 
less /var/log/maillog 
echo "testing postfix server email" | mail -s "Real test email" markuj5@gmail.com
echo "testing postfix server email" | mail -s "Real test email" Andris.Sivins@knab.gov.lv
echo "testing postfix server email" | mail -s "Real test email" Janis.Kulmanis@knab.gov.lv
echo "testing postfix server email" | mail -s "Real test email" janis.it.mikelsons@knab.gov.lv
clear
postqueue -p
echo "test message" | mail -s "Test email" student@localhost
postqueue -p
postqueue -f
df-h
df -h
vi /etc/aliases
postalias /etc/aliases
newaliases
vi /etc/aliases
echo "test message" | mail -s "Test email" admins@localhost
mutt
less /var/spool/mail/student 
dnf install dovecot
vi /etc/dovecot/dovecot.conf 
vi /etc/dovecot/conf.d/10-mail.conf 
systemctl restart dovecot
id student
usermod -aG mail student
id student
mutt -f imap://student@centos8-1
vi /etc/dovecot/conf.d/10-mail.conf 
vi /etc/dovecot/conf.d/10-ssl.conf 
mv /etc/pki/dovecot/private/dovecot.pem /etc/pki/dovecot/private/dovecot.old.pem
mv /etc/pki/dovecot/certs/dovecot.pem /etc/pki/dovecot/certs/dovecot.old.pem
vi /etc/pki/dovecot/dovecot-openssl.cnf 
cd /usr/share/doc/dovecot/
ls -la
bash mkcert.sh 
mutt -f imaps://student@centos8-1
cat /etc/postfix/main.cf | grep -i inet_interfaces
cat /etc/postfix/main.cf | grep -i inet_interfaces | grep -v "#"
postconf -e 'inet_interfaces = localhost'
cat /etc/postfix/main.cf | grep -i inet_interfaces | grep -v "#"
postconf -e 'inet_interfaces = all'
cat /etc/postfix/main.cf | grep -i inet_interfaces | grep -v "#"
clear
cd
cd lfs311_Nov/
history
history | awk '$1 > 1000' | cut -c 8- > /root/lfs311_Nov/day3-hisotry.md 
git add .
git commit -m "Adding day3 file"
git push
clear
cd
dnf install vsftpd
mkdir -m 730 /var/ftp/uploads
chown root.ftp /var/ftp/uploads
ls -la /var/ftp/uploads
vi /etc/vsftpd/vsftpd.conf 
echo "testfile" > testfile.txt
cat testfile.txt
systemctl start vsftpd.
systemctl start vsftpd.service 
systemctl status vsftpd.service 
ftp 192.168.1.81
ls -la /var/ftp/uploads/
groupadd sales
chgrp /var/ftp/uploads/ sales
chgrp sales /var/ftp/uploads/ 
chmod 2740 /var/ftp/uploads/
ls -la /var/ftp/uploads/
chmod 2770 /var/ftp/uploads/
ls -la /var/ftp/uploads/
cp testfile.txt testfile2.txt 
ftp 192.168.1.81
id student
usermod -aG sales student
id student
ftp 192.168.1.81
usermod -aG ftp student
ftp 192.168.1.81
chmod 2773 /var/ftp/uploads/
ls -la /var/ftp/uploads/
ftp 192.168.1.81
chmod 730 /var/ftp/uploads/
chown root.ftp /var/ftp/uploads/
ftp 192.168.1.81
ls
ftp 192.168.1.81
ls -la /var/ftp/uploads/
cd /var/ftp
ls -la
dnf install rsync
mkdir /tmp/rsync_files
ls -la /tmp/rsync_files
cd
cd /tmp/rsync_files/
ls
rsync -av /tmp/rsync_files/* root@centos8-2:/tmp/source/
rsync
ls -la
rsync -av  root@centos8-2:/tmp/source/ /tmp/rsync_files/*
ls -la
rm \*/
rm \*/ -rf
rsync -av  root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av  root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rm -rf *
ls -la
rsync -av --no-owner root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av --no-owner --exclude config.yml root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rm -rf *
rsync -av --no-owner --exclude config.yml root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av --no-owner --exclude config.yml root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av --no-owner --exclude config.yml --delete root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av --no-owner --exclude config.yml --delete root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rsync -av --no-owner --no-perms --exclude config.yml --delete root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
rm -rf *
ls -la
rsync -av --no-owner --no-perms --exclude config.yml --delete root@centos8-2:/tmp/source/ /tmp/rsync_files/
ls -la
vi /etc/rsync.conf
rm -rf *
ls -la
systemctl status rsyncd
dnf install rsyncd
dnf install rsync
rsync -av
dnf install rsync-daemon
systemctl status rsyncd.s
systemctl status rsyncd
systemctl start rsyncd
systemctl status rsyncd
ls -la
vi /etc/rsyncd.conf 
rsync -av
systemctl restart rsyncd.s
systemctl restart rsyncd
ls -la
rsync localhost::
ls -la
cd
clear
cd /tmp/rsync_files/
ls -la
rsync -t rsync://
rsync --daemon 
ls -la
vi /etc/rsync.conf 
vi /etc/rsyncd.conf 
systemctl restart rsyncd.service 
systemctl restart rsyncd.socket 
systemctl status rsyncd.socket 
ls -la
clear
cd
clear
dnf install squid
vi /etc/squid/squid.conf
squid -k parse
vi /etc/squid/whitelist.txt
squid -k parse
vi /etc/squid/squid.conf
squid -k parse
systemctl restart squid.service 
vi /etc/squid/whitelist.txt
squid -k reconfigure
systemctl restart squid.service
vi /etc/squid/whitelist.txt
vi /etc/squid/squid.conf
systemctl restart squid.service
vi /etc/squid/squid.conf
systemctl restart squid.service
vi /etc/squid/squid.conf
systemctl restart squid.service
clear
dnf install nfs-utils
mkdir -m 755 /srv/nfs_{pub,group,secure}
chown nfsnobody:nfsnobody /srv/nfs_pub/
chown nobody:nobody /srv/nfs_pub/
groupadd devops
chgrp devops /srv/nfs_group/
chmod -R 2770 /srv/nfs_group/
usermod -aG devops student
useradd peter
chown peter /srv/nfs_secure/
vi /etc/exports
exportfs -rav
showmount -e 192.168.1.81
systemctl status nfs
systemctl status nfs-server.service 
systemctl start nfs-server.service 
systemctl status nfs-server.service 
showmount -e 192.168.1.81
cd /srv/nfs_pub/
ls -la
vi /etc/exports
exportfs -rav
ls -la
vi /etc/exports
ls -la ../nfs_group/
id devops
id peter
usermod -aG devops peter
id peter
cd
cd /srv/
ls -la
useradd lisa
id lisa
chown lisa:devops nfs_group/
ls -la 
exportfs -rav
history
cd
vi lfs311_Nov/day3-hisotry.md 
history | awk '$1 > 1000' | cut -c 8- 
vi lfs311_Nov/day3-hisotry.md 
cat lfs311_Nov/day3-hisotry.md | wc -l
history | awk '$1 > 1000' | cut -c 8- > /root/lfs311_Nov/day3-hisotry.md
cat lfs311_Nov/day3-hisotry.md | wc -l
vi /root/lfs311_Nov/day3-hisotry.md
cd lfs311_Nov/
git add .
git commit -m "Day3 history"
git push
cd
dnf install samba smaba-client
dnf install samba samba-client
systemctl enable --now smb
smbclient -L localhost
mkdir /srv/smbshare
chmod 777 /srv/smbshare
vi /etc/samba/smb.conf
mv /srv/smbshare/ /srv/smb-ro
tesparm
testparm
cd /srv/smb-ro/
touch file1
df -h > file1 
cat file1 
vi /etc/samba/smb.conf
cd
cd /srv/
ls -la
mkdir private
chmod 2777 private
chgrp devops private/
id lisa
usermod -aG devops lisa
ud lisa
id lisa
id peter
usermod -G peter
usermod -G peter peter
id peter
smbpasswd -a lisa
smbpasswd -a peter
testparm
ls -la
chmod 2770 private
systemctl restart smb.service 
ls -la
chmod 2774 private
systemctl restart smb.service 
cd private/
ls -la
cd ..
chmod 2775 private
systemctl restart smb.service 
vi /etc/samba/smb.conf
cd
history
history | awk '$1 > 1000' | cut -c 8- > /root/lfs311_Nov/day3-hisotry.md
