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
