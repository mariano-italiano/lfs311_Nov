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
