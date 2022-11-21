systemctl status sshd
systemctl disable sshd
systemctl status sshd
vi /etc/systemd/system/multi-user.target.wants/sshd.service.
runlevel
systemctl enable --now ssd
systemctl enable --now sshd
systemctl status sshd
clear
timedatectl 
journalctl -b
ifconfig 
ip
ip a s
ifconfig 
ip a a 192.168.2.100 dev ens160
ifconfig 
clear
ifconfig 
ip a s
ls -la /lib/systemd/system/runlevel*.target
ls -la /lib/systemd/system/multi-user.target
vi /lib/systemd/system/multi-user.target
systemctl isolate 6
systemctl isolate reboot.target 
ls -la /lib/systemd/system/
ls -la /etc/systemd/system/
ls -la /run/systemd/system/
systemctl get-default 
systemctl set-default multi-user.target 
systemctl list-units --type target
systemctl list-units --type target --all
systemctl list-units --type socket --all
history
clear
ip a s
lsmod
lsmod | grep vmxnet
lsmod | sort
modinfo vmxnet3
modinfo e1000
lsmod | grep dm_crypt
modprobe dm_crypt
lsmod | grep dm_crypt
vi /etc/modprobe.d/kvm.conf 
modprobe --help
modprobe -r dm_crypt
lsmod | grep dm_crypt
find /lib/modules -name *dm_crypt*
find /lib/modules -name dm_crypt*
find /lib/modules -name dm_crypt
find / -name "*dm_crypt*"
find / -name "*vmxnet*"
cd /etc/udev/
ls -la
less udev.conf
cd rules.d
ls -la
vi 70-persistent-ipoib.rules
vi 70-custom-ifname.rules
cat 70-persistent-ipoib.rules
vi 70-custom-ifname.rules
ip a 
vi 70-custom-ifname.rules
ip link list
reboot
ip a s
nmtui
ip a s
ip a 
vi 70-custom-ifname.rules
cd /etc/udev/
vi 70-custom-ifname.rules
cd rules.d/
vi 70-custom-ifname.rules
rm 70-custom-ifname.rules 
vi /etc/systemd/
cd /etc/systemd/
ls
mkdir network
vi network/70-cutom-ifname.link
vi /lib/systemd/network/99-default.link 
vi network/70-cutom-ifname.link
vi network/70-custom-ifname.link
ip a s
reboot
ip a
vi /etc/sysconfig/network-scripts/ifcfg-ens160 
ip route
route -n
ip route add 172.16.1.0/24 via 192.168.1.254
route -n
ip route add 172.16.2.0/24 via 172.20.1.1
ip route add 172.20.1.1/32 via 192.168.254
ip route add 172.20.1.1/32 via 192.168.1.254
ip route add 172.16.2.0/24 via 172.20.1.1
route -n
vi /etc/sysconfig/network-scripts/route-eth0
reboot
ip a s
vi /etc/sysconfig/network-scripts/ifcfg-Wired_connection_1 
nmtui
ip a s
nmtui
ip a s
route -n
vi /etc/sysconfig/network-scripts/route-eth0 
cp /etc/sysconfig/network-scripts/route-eth0 /etc/sysconfig/network-scripts/route-ens160
reboot
route -n
rm /etc/sysconfig/network-scripts/route-ens160
rm /etc/sysconfig/network-scripts/route-eth0 
vi /etc/hostname 
hostnamectl set-hostname centos8-new
vi /etc/hostname 
hostnamectl set-hostname centos8-1
vi /etc/resolv.conf 
ping vmware.com
nslookup vmware.com
nmcli connection down Wired\ connection\ 2 ; nmcli connection up Wired\ connection\ 2
vi /etc/resolv.conf 
nmcli-edit
nmtui-edit 
nmcli connection down eth0 ; nmcli connection up eth0 
ip a s
route -n
nmtui
ls -la /etc/sysconfig/network-scripts/route-Wired_connection_2 
vi /etc/sysconfig/network-scripts/route-Wired_connection_2
ip a s
ip r s
ip link 
ip link show
ip link set eth0 mtu 900
ip link show
ip link set eth0 mtu 9000
ip link show
ip link set eth0 mtu 1500
nmtui-edit 
nmtui
nmtui-edit 
nmcli 
nmcli connection show
ls -la
ls -lai
nmcli connection show
nmcli device show
nmcli device show eth0
nmcli device status
nmcli connection add con-name Internet ifname eth0 type ethernet ip4 192.168.1.199 gw4 192.168.1.1
nmcli connection show
ip a s
nmcli connection delete Internet 
nmcli connection add con-name Internet ifname ens224 type ethernet ip4 192.168.1.199 gw4 192.168.1.1
nmcli connection show
nmcli connection down Wired\ connection\ 1 
nmcli connection show
ip a s
nmcli connection show
nmcli connection modify 
nmcli connection modify Wired\ connection\ 1 ipv4.addresses 192.168.1.190
nmcli connection edit 
nmcli connection edit Wired\ connection\ 1 
history
ls -la
less .nmcli-history
nmcli connection show
nmcli connection show Wired\ connection\ 1 
nmcli connection modify Wired\ connection\ 1 connection.id ExtraOne
nmcli connection show
nmcli connection show ExtraOne
nmcli connection show ExtraOne | wc -l
nmtui-edit 
git clone https://github.com/mariano-italiano/lfs311_Nov.git
cd lfs311_Nov/
ls
history 
history | awk '$1' > 793 | cut -c 8-
history | awk '$1 > 793' | cut -c 8-
history | awk '$1 > 793' | cut -c 8- > day1-hisotry.md
git status
rm 793 
git status
ls -la
rm 793
ls -la
git status
git add day1-hisotry.md 
git commit -m "Adding day1 file"
git config --global user.email "markuj5@gmail.com"
git config --global user.name "Marcin"
git commit -m "Adding day1 file"
git push
ls -la
cd
nmcli connection show
nmcli connection delete ExtraOne 
nmcli connection delete Internet 
nmcli connection show
reboot
ip a s
netstat -vatnulp
watch netstat -vatnulp
ip a s
clear
ping 192.168.1.1
ping 192.168.1.1 -c 4
traceroute google.com
traceroute google.com -I 
traceroute --help
q
traceroute google.com -I 
traceroute google.com 
nmap --help
nmap 192.168.1.81
telnet 192.168.1.1 443
telnet 192.168.1.1 80
telnet 192.168.1.1 22
curl -v telnet://192.168.1.1:443
netstat -tuvalpn
netstat -tuvalp
clear
netstat -tuvalpn
netstat -tuvalpn|grep chrony
ss
ss -vatunlp
ss -atunlp
netstat -tuvalpn
clear
arp
rarp
arp -hhelp
arp -a
dnf install rarp
dnf provides *rarp*
arp
clear
tcpdump -i eth0 -nn -s0 -v port 22
systemctl status chronyd
cat /etc/services | grep ntp
cat /etc/services | grep samba
cat /etc/services | grep winbind
cat /etc/services | grep kerberos
cat /etc/services | grep rdp
cat /etc/services | grep 3128
tcpdump -i eth0 -nn -s0 -v port 123
vi /etc/ssh/sshd_config 
systemctl restart sshd
tcpdump -i eth0 -nn -s0 port 2222
tcpdump -i eth0 -nn -s0 port 2222 -w ssh2222.pcap
ls
tcpdump -A -s0 port 123
tcpdump -A -s0 port 123 -v
tcpdump -A -s0 port 22
tcpdump -i eth0 udp
tcpdump -i eth0 udp port 123
tcpdump -i eth0 host 192.168.1.1
tcpdump -i eth0 host 192.168.1.1 -w gw.pcap
sysctl 
sysctl -a
sysctl -a | ipv4
sysctl -a | grep ipv4
sysctl -a | grep forward
sysctl -a | grep icmp
vi /etc/sysctl.conf 
sysctl -p
vi /etc/sysctl.conf 
sysctl -p
ping 192.168.1.81
vi /etc/sysctl.conf 
sysctl -p
ping 192.168.1.81
sysctl -a | grep arp
nc --help
nc -l 5555
nc -v -w 2 -z 192.168.1.82 80
nc -v -w 2 -z 192.168.1.82 22
nc -v -w 2 -z 192.168.1.82 20-40
nc -v -w 2 -z 192.168.1.82 22 123
nc -v -n 192.168.1.82 22
nslookup centos8
nmtui-edit 
nslookup centos8
nmcli connection down eth0 ;nmcli connection up eth0 
nslookup centos8
nslookup home
nslookup centos8.home
nslookup wp.pl
nslookup google.com
nslookup 
nslookup google.com
nslookup 142.250.75.14
nslookup  smtp.google.com
dig google.com
dig -t mx google.com
timedate
timedatectl 
hwclock 
timedatectl set-timezone Europe/Riga 
timedatectl 
date
timedatectl list-timezones 
timedatectl set-ntp no
timedatectl 
timedatectl set-ntp yes
timedatectl 
dnf install chronyd
dnf install chrony
vi /etc/chrony.conf 
cat /etc/chrony.conf | grep -v "#"
vi /etc/chrony.conf 
systemctl restart chronyd
chronyc sources
watch chronyc sources
chronyc sources
chronyc --help
chronyc sources -n
chronyc sources -d
chronyc -d sources 
chronyc -n sources 
chrony trcking
chronyc trcking
chronyc tracking
chronyc sources 
systemctl stop chronyd
dnf install ntpd
dnf install ntp
systemctl start chronyd
vi /etc/ssh/sshd_config 
pwd
ls -la
ls -la /home/student
vi /etc/hosts
ping centos8-2
ssh-keygen -t
ssh-keygen -t rsa
ls -la 
cd .ssh/
ls -la
cd
ssh-copy-id root@192.168.1.82
ssh centos8-2
ip a s
vi /etc/resolv.conf 
vi /etc/hosts
ssh centos8-2
cat .ssh/id_rsa.pub 
ssh --help
man ssh
ssh -Nf 2222:192.168.1.81:22 student@192.168.1.82
ssh -Nf -L 2222:192.168.1.81:22 student@192.168.1.82
vi /etc/resolv.conf 
vi /etc/ssh/sshd_config 
sysctl -a | grep forward
vi /etc/sysctl.
vi /etc/sysctl.conf 
sysctl -p
ssh -Nf -L 2222:192.168.1.81:22 student@192.168.1.82
sysctl -p
ssh -Nf -L 2222:192.168.1.81:22 student@192.168.1.82
ssh -Nf -L 2220:192.168.1.81:22 student@192.168.1.82
netstat -vatnlp 
systemctl restart sshd
netstat -vatnlp 
ssh -p 2220:localhost
ssh -p 2220 localhost
reboot
netstat -vatnlp 
ssh -Nf -L 2222:192.168.1.82:22 student@192.168.1.81
netstat -vatnlp 
ssh -p 2222 localhost
dnf install pssh
vi hosts
ssh-copy-id centos8-1
pssh -i -h hosts "date;hostname"
vi script.sh
chmod +x script.sh 
scp script.sh centos8-1:/tmp
scp script.sh centos8-2:/tmp
pssh -i -h hosts "/tmp/script.sh"
vi /etc/ssh/sshd_config 
init 5
ps -ef | grep ssh
kill -15 1418
ps -ef | grep ssh
dnf install tigervnc tigervnc-server
vncserver 
vncviewer localhost:5901
history
history | awk '$1 > 612' | cut -c 8-
history | awk '$1 > 612' | cut -c 8- | wc -l
history | awk '$1 > 612' | cut -c 8- > lfs311_Nov/day1-hisotry.md 
