## wireguard-install
WireGuard [road warrior](http://en.wikipedia.org/wiki/Road_warrior_%28computing%29) installer for Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS and Fedora.

This script will let you set up your own VPN server in no more than a minute, even if you haven't used WireGuard before. It has been designed to be as unobtrusive and universal as possible.

### Installation
Run the script and follow the assistant:

`wget https://git.io/wireguard -O wireguard-install.sh && bash wireguard-install.sh`

Once it ends, you can run it again to add more users, remove some of them or even completely uninstall WireGuard.

### I want to run my own VPN but don't have a server for that
You can get a VPS from just $1/month at [VirMach](https://billing.virmach.com/aff.php?aff=4109&url=billing.virmach.com/cart.php?gid=18).

### Donations

If you want to show your appreciation, you can donate via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VBAYDL34Z7J6L) or [cryptocurrency](https://pastebin.com/raw/M2JJpQpC). Thanks!



//unbuntu 20.4(腾讯轻应用服务器）

52:  
//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.52/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.52.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.52.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.52.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.52.22    -p tcp --dport 80  -j SNAT --to-source 10.10.52.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.52.22:22  






53:  
//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.53/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh   
service wg-quick@wg0 restart  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.53.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.53.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.53.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.53.22    -p tcp --dport 80  -j SNAT --to-source 10.10.53.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.53.22:22  




54:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.54/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.54.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.54.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.54.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.54.22    -p tcp --dport 80  -j SNAT --to-source 10.10.54.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.54.22:22  



55:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.55/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.55.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.55.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.55.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.55.22    -p tcp --dport 80  -j SNAT --to-source 10.10.55.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.55.22:22  





56:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.56/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.56.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.56.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.56.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.55.22    -p tcp --dport 80  -j SNAT --to-source 10.10.56.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.56.22:22  




57:

55:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.57/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.57.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.57.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.57.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.55.22    -p tcp --dport 80  -j SNAT --to-source 10.10.57.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.57.22:22  




58:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.58/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.58.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.58.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.58.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.55.22    -p tcp --dport 80  -j SNAT --to-source 10.10.58.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.58.22:22  




59:  

//安装  
wget https://raw.githubusercontent.com/wbug/wireguard-install/master/wireguard-install.sh -O wireguard-install.sh  
sed -i "s/10.7.0/10.10.59/g" \`grep 10.7.0 -rl ./wireguard-install.sh\`   
chmod +x wireguard-install.sh  
./wireguard-install.sh  
  
//restart .. 最好保存为  restart.sh  
service wg-quick@wg0 restart
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.59.22:44158  
iptables -t nat -I PREROUTING -p udp -d 10.0.4.??  --dport 44158 -j DNAT --to 10.10.59.22:44158  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44180 -j DNAT --to 10.10.59.22:80  
iptables -t nat -A POSTROUTING  -d 10.10.55.22    -p tcp --dport 80  -j SNAT --to-source 10.10.59.1  
iptables -t nat -I PREROUTING -p tcp -d 10.0.4.??  --dport 44122 -j DNAT --to 10.10.59.22:22  








