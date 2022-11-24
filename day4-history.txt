iptables -P OUTPUT ACCEPT
iptables -L -v -n 
iptables -F
iptables -t nat -F
iptables -t nat -L -v -n
iptables -L -v -n
nft list table inet filter_it
nft list table inet filter
nft -h
nft list tables
nft list table inet filter
nft add table inet myfilter
nft add chain inet myfilter input_stuff { type filter hook input priority 0 \; }
nft add rule inet myfilter input_stuff tcp dport 22 accept
nft add rule inet myfilter input_stuff udp sport 53 accept
nft list table inet myfilter
nft add rule inet myfilter input_stuff ct state established,related accept
nft add rule inet myfilter input_stuff counter
nft list table inet myfilter
nft add rule inet myfilter input_stuff iifname lo accept
nft add rule inet myfilter input_stuff drop
nft list table inet myfilter
mkdir /etc/nftables
ls -la /etc/nftables
nft list table inet myfilter > /etc/nftables/myfilter.nft
cat /etc/nftables/myfilter.nft
nft flush ruleset
nft list table inet myfilter
nft -f /etc/nftables/myfilter.nft
nft list table inet myfilter
systemctl status firewalld.service 
systemctl status nftables.service 
systemctl enable --now  nftables.service 
nft list table inet myfilter
nft list table 
nft list tables
dnf install rsyslog
vi /etc/rsyslog.conf 
systemctl restart rsyslog.service 
vi /etc/rsyslog.d/custom-logging.conf
systemctl restart rsyslog.service 
cd /var/log
ls -la
systemctl status nftables.service 
systemctl disable --now -la
systemctl disable --now nftables.service 
systemctl disable --now iptables
vi /etc/rsyslog.conf 
vi /etc/rsyslog.d/custom-logging.conf 
systemctl restart rsyslog.service 
ls -la
less centos8-2-logs.txt
vi /etc/rsyslog.d/custom-logging.conf 
systemctl restart rsyslog.service 
ls -la
ls centos8-2
ls centos8-2 -la
less centos8-2/systemd.log 
less centos8-2/sshd.log 
vi /etc/rsyslog.d/custom-logging.conf 
systemctl restart rsyslog.service 
ls -la
ls -la centos*
less centos7.log 
less centos8.log 
less centos7.log 
ping 192.168.1.80
ip a a 192.168.1.80/24 dev eth0
ip a 
ping 192.168.1.80
vi /etc/hosts
dnf install pacemaker corosync pcs
dnf install pacemaker corosync
dnf install pcs
dnf install pacmaker
dnf install pacemaker
dnf install corosync
dnf install corosync --nobest
dnf install corosync --nobest --skip-broken
dnf install pcs
vi /etc/yum.repos.d/CentOS-Linux-HighAvailability.repo 
dnf install corosync pcs pacemaker
systemctl start pcsd
systemctl enable pacemaker.service  corosync pcsd
passwd hacluster
pcs host auth  centos8-1
pcs host auth  centos8-2
pcs cluster  setup webcluster centos8-1 centos8-2
pcs cluster status
pcs cluster start --all
pcs cluster status
pcs property set stonith-enabled=false
pcs property set no-quorum-policy=ignore
pcs cluster status
pcs resource create virtual_ip ocf:heartbeat:httpd configfile:/etc/httpd/httpd.conf op monitor timeout="5s" interval="5s"
pcs resource create virtual_ip ocf:heartbeat:httpd configfile=/etc/httpd/httpd.conf op monitor timeout="5s" interval="5s"
pcs resource create virtual_ip ocf:heartbeat:http configfile=/etc/httpd/httpd.conf op monitor timeout="5s" interval="5s"
pcs resource create virtual_ip ocf:heartbeat:nginx configfile=/etc/httpd/httpd.conf op monitor timeout="5s" interval="5s"
pcs status resources
systemctl status httpd
systemctl start resources
systemctl start httpd
systemctl status httpd
pcs status resources
pcs resource delete virtual_ip
pcs resource create virtual_ip ocf:heartbeat:IPaddr2 ip=192.168.1.80 cidr_netmask=32 op monitor interval=30s
pcs status resources
pcs resource create webserver ocf:heartbeat:nginx configfile=/etc/httpd/httpd.conf op monitor interval=5s timeout=5s
pcs status resources
pcs cluster status
pcs status resources
clear
dnf install mariadb-server
systemctl start mariadb
mysql_secure_installation 
mysqladmin -u root -p version
cd
mysql -u root 
mysql -u root -p
mysql -u sqladmin -p myDB
vi showdetails
df -h 
uptime
uptime | cut -d " " -f3
uptime | cut -d " " -f4
uptime | cut -d " " -f5
uptime | awk -F' ' '{print $2}'
uptime | awk -F' ' '{print $3}'
uptime | cut -d " " -f5 | awk -F',' '{print $1}'
vi showdetails 
chmod +x showdetails 
./showdetails 
vi showdetails 
./showdetails 
vi showdetails 
./showdetails 
vi showdetails 
./showdetails 
dnf install rpmdevtool rpmlint
dnf install rpmdevtools rpmlint
rpmdev-setuptree
ls -la
cd rpmbuild
ls -la
tree
vi SPECS/admin-scripts-1.0.spec
mkdir -p SOURCES/admin-scripts-1.0/scripts
cp ../showdetails SOURCES/admin-scripts-1.0/scripts/
ls -la SOURCES/admin-scripts-1.0/scripts/
cd SOURCES/
tar -cfz admin-scripts-1.0.tar.gz admin-scripts-1.0
ls -la
tar -czf admin-scripts-1.0.tar.gz admin-scripts-1.0
rm z 
ls -la
rpmlint ../SPECS/admin-scripts-1.0.spec 
cd ..
rpmbuild --bb rpmbuild/SPECS/admin-scripts-1.0.spec
vi rpmbuild/SPECS/admin-scripts-1.0.spec
rpmbuild --bb rpmbuild/SPECS/admin-scripts-1.0.spec
tree rpmbuild/
rpm -ivh rpmbuild/RPMS/noarch/admin-scripts-1.0-0.noarch.rpm 
showdetails 
which showdetails
rpm -qi admin-scripts
rpm -qi netstat
rpm -qi telnet
rpm -e admin-scripts 
showdetails
dnf groupinstall "Development Tools" 
dnf groupinstall "Development Tools" --allowerasing
vi hello.c
gcc hello.c -o hello
./hello 
rm hello
vi configure.ac
vi Makefile.am
autoconf
aclocal
autoconf
automake --add-missing
./configure 
make
vi Makefile.in 
ls -la
./hello 
history
history | awk '$1 > 1382' | cut -c 8- > /root/lfs311_Nov/day4-hisotry.md
