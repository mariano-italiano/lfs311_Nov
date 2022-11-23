dnf install bind
vi /etc/named.conf 
dnf install unbound
vi /etc/unbound/unbound.conf 
systemctl start unbound
unbound-checkconf 
systemctl status unbound
netstat -vatnulp | grep 53
vi /etc/unbound/unbound.conf 
systemctl restart unbound
vi /etc/unbound/unbound.conf 
systemctl restart unbound
systemctl status unbound
systemctl status libvirtd
vi /etc/resolv.conf 
nslookup google.com
vi /etc/unbound/unbound.conf 
systemctl restart unbound
systemctl status libvirtd
systemctl status unbound
vi /etc/resolv.conf 
nslookup google.com
nslookup wp.pl
vi /etc/unbound/unbound.conf 
systemctl restart unbound
systemctl status unbound
nslookup google.com
systemctl status firewalld.service 
vi /etc/resolv.conf 
nslookup google.com
vi /etc/resolv.conf 
nslookup google.com
ip a 
vi /etc/unbound/unbound.conf 
systemctl restart unbound
vi /etc/resolv.conf 
nslookup google.com
vi /etc/hosts
nslookup google.com
vi /etc/nsswitch.conf
vi /etc/hosts
ping google.com
vi /etc/nsswitch.conf
ping google.com
vi /etc/nsswitch.conf
ping centos8-2
dnf install bind
vi /etc/named
vi /etc/named.conf 
cp -rp /var/named/named.localhost /var/named/lab.local.zone
vi /var/named/lab.local.zone
vi /etc/resolv.conf 
systemctl start named
systemctl status named
vi /var/named/lab.local.zone
vi /etc/named.conf 
cp -rp /var/named/lab.local.zone /var/named/1.168.192.in-addr.arpa.zone
vi /var/named/1.168.192.in-addr.arpa.zone
systemctl restart named
systemctl status named
vi /etc/named.conf
systemctl restart named
systemctl status named
vi /etc/named.conf 
systemctl restart named
systemctl status named
vi /etc/named.conf 
systemctl restart named
systemctl status named
vi /etc/named.conf 
cd /var/named
mv lab.local.zone lab-ext.local.zone 
cp -rp lab-ext.local.zone lab-int.local.zone 
vi lab-int.local.zone
systemctl restart named
vi /etc/named.conf 
cd
ip a
ip a a 192.168.1.181/24 dev eth0
ipa
ip a 
vi /etc/hosts
vi /etc/resolv.conf 
vi /etc/hosts
dnf install httpd -y
dnf install elink lynx mod_ssl
dnf install elinks lynx mod_ssl
dnf install mod_ssl
y
clear
systemctl start httpd
vi /var/www/html/index.html
mkdir -p /web/{sales,account}
ls -la /web
getenforce 
ls -lZ /var/www/html/
cd /web/account/
cp -rp /var/www/html/index.html .
vi index.html 
cd
vi /etc/httpd/conf/httpd.conf 
vi /etc/httpd/conf.d/account.conf
systemctl restart httpd
lynx -dump http://account.lab.local
lynx -dump http://localhost
vi /etc/host
vi /etc/hosts
vi /etc/httpd/conf.d/account.conf
vi /etc/hosts
vi /etc/httpd/conf.d/account.conf
systemctl restart httpd
lynx -dump http://account.lab.local
lynx -dump http://localhost
vi /etc/hosts
cp -rp /etc/httpd/conf.d/account.conf /etc/httpd/conf.d/sales.conf
vi /etc/httpd/conf.d/sales.conf
systemctl restart httpd
systemctl status httpd
vi /etc/httpd/conf.d/sales.conf
systemctl restart httpd
lynx -dump http://account.lab.local
lynx -dump http://localhost
lynx -dump http://sales.lab.local
cp -rp /web/account/index.html  /web/sales/
vi /web/sales/index.html 
lynx -dump http://sales.lab.local
lynx -dump http://account.lab.local
lynx -dump http://localhost
lynx -dump http://sales.lab.local
vi /etc/httpd/conf.d/sales.conf
systemctl restart httpd
cat /etc/hosts
vi /etc/httpd/conf.d/sales.conf
systemctl restart httpd
mkdir /web/sales/secure
htpasswd -c /etc/httpd/creds peter
ls -la /etc/httpd/creds
cat /etc/httpd/creds
vi /etc/httpd/conf.d/sales.conf 
systemctl restart httpd
cd /web/sales/secure/
ls
touch file1
mkdir sec1
vi /etc/httpd/conf.d/sales.conf 
ls -la /web/sales/
vi /etc/httpd/conf.d/sales.conf 
systemctl restart httpd
vi /etc/httpd/conf.d/sales.conf 
htpasswd -c /etc/httpd/credentials lisa
vi /etc/httpd/conf.d/sales.conf 
mkdir /web/sales/protected
mkdir /web/sales/protected/folder1
touch /web/sales/protected/sensitivedata1
systemctl restart httpd
vi /etc/httpd/conf.d/sales.conf 
systemctl restart httpd
vi /etc/httpd/conf.d/sales.conf 
systemctl restart httpd\
systemctl restart httpd
vi /etc/httpd/conf.d/sales.conf 
vi /etc/httpd/conf.d/ssl.conf 
mv /etc/pki/tls/private/localhost.key /etc/pki/tls/private/localhost.key.origin
openssl genrsa -aes128 2048 > /etc/pki/tls/private/localhost.key
openssl req -utf8 -new -key /etc/pki/tls/private/localhost.key -x509 -days 365 -out /etc/pki/tls/certs/localhost.crt
systemctl restart httpd
openssl req -utf8 -new -key /etc/pki/tls/private/localhost.key-out /tmp/sales.lab.local.csr
openssl req -utf8 -new -key /etc/pki/tls/private/localhost.key-out -x509 /tmp/sales.lab.local.csr
openssl req -utf8 -new -key /etc/pki/tls/private/localhost.key-out -out /tmp/sales.lab.local.csr
openssl req -utf8 -new -key /etc/pki/tls/private/localhost.key -out /tmp/sales.lab.local.csr
ls -la
ls -la /tmp/
vi /etc/httpd/conf/httpd.conf 
vi /etc/httpd/conf/
vi /etc/httpd/conf.modules.d/
vi /etc/httpd/conf.modules.d/00-base.conf
cat /etc/httpd/conf.modules.d/00-base.conf | grep rewrite
cat /etc/httpd/conf.modules.d/00-base.conf | grep alias
cat /etc/httpd/conf.modules.d/00-base.conf | grep status
httpd -V
httpd -h
httpd -l
httpd -M
httpd -M | sort | rewrite
httpd -M | sort | grep -i rewrite
httpd -M | sort | grep -i alias
httpd -M | sort | grep -i status
cd
mkdir /new-cgi
vi /new-cgi/script.cgi
chmod +x /new-cgi/script.cgi
/new-cgi/script.cgi
/new-cgi/script.cgi 123
vi /new-cgi/script.cgi
cd /web/sales/
ls
mv /new-cgi/script.cgi .
lynx -dump http://sales.lab.local
vi /etc/httpd/conf.d/sales.conf 
systemctl restart httpd

vi /etc/httpd/conf.d/scripts.conf
lynx -dump http://sales.lab.local
lynx -dump http://localhost/scripts/script.cgi?12345
lynx -dump http://sales.lab.local/scripts/script.cgi?12345
vi /etc/httpd/conf.d/scripts.conf
lynx -dump http://sales.lab.local/scripts/script.cgi?12345
ls
rm script.cgi 
ls
cd /new-cgi/
ls
vi script.cgi
chmod +x script.cgi
./script.cgi 1234
vi script.cgi
./script.cgi 1234
lynx -dump http://sales.lab.local/scripts/script.cgi?12345
lynx -dump http://localhost/scripts/script.cgi?12345
cd
vi /etc/httpd/conf.d/scripts.conf 
ls -la /new-cgi/
./script.sh 1234
vi /etc/httpd/conf.d/scripts.conf 
vi /new-cgi/script.cgi 
/new-cgi/script.sh 1234
/new-cgi/script.sh
cd /new-cgi/
ls
ls -la
./script.cgi 123
lynx -dump http://localhost/scripts/script.cgi?12345
lynx -dump http://192.168.1.81/scripts/script.cgi?12345
lynx -dump http://192.168.1.181/scripts/script.cgi?12345
cat script.cgi 
vi /etc/httpd/conf.d/sales.conf 
mkdir /web/sales/server-status
systemctl restart httpd
