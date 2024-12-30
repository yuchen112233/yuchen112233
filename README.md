iptables -t filter -F
iptables -t nat -F
iptables -t mangle -F
LOCAL_FILE="/data/local/tmp/excc24.dat"
current_date=$(date +"%Y-%m-%d %H:%M:%S")
echo " "
echo "[32m$current_date[0m"
echo " "
echo "[32mTELEGRAM @EXCC24[0m"
echo " "
correct_hash="9c679beba434bcc304b2d104225b475445f50efd52f7315b11a299382a8e07e9"
echo -n "钥匙 / KEY: "
read -s user_password
echo
user_hash=$(echo -n "$user_password" | sha256sum | awk '{ print $1 }')
if [ "$user_hash" == "$correct_hash" ]; then
echo "加载中 / LOADING..."
sleep 4  # Loading selama 3 detik
echo "结束 / FINISH"
else
echo "Password salah. Akses ditolak!"
exit 1
fi
clear
echo "
███████╗██╗  ██╗ ██████╗
██╔════╝╚██╗██╔╝██╔════╝
█████╗   ╚███╔╝ ██║
██╔══╝   ██╔██╗ ██║
███████╗██╔╝ ██╗╚██████╗
╚══════╝╚═╝  ╚═╝ ╚═════╝
"
echo  "[32m                   JOIN TELEGRAM @EXCC24"
echo " "
echo "=============================================================="
echo "             INTERCEPT ARENA BREAKOUT INTERNATIONAL 1.181"
echo "             USE DECRYPT ESP"
echo "             Version $VERSION"
echo " "
echo "                   反馈 / FEEDBACK @buuzlighty"
echo " "
echo "             expired date : $expiration_date"
echo "             current date : $current_date"
echo "=============================================================="
echo -e "[32m(keyboard Input) 1 开启拦截规则飞 (Turn On) @excc24 [0m"
echo -e "[32m(Keyboard Input) 2 清除规则飞机群 (Turn Off) @excc24 [0m"
read num
if [ "$num" == "1" ]; then
iptables -A OUTPUT -m string --string "listdl" --algo bm --to 65535 -j DROP
iptables -A INPUT -p tcp -m string --string "down.anticheatexpert.com" --algo bm --to 65535 -m tcp --dport 443 -j DROP
iptables -A INPUT -m string --string "data|zip|ano|config|SpeedUp|cache" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "unzipmrpcs.data" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "cache" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "SpeedUp" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "mrpcs_a_s.data" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "config" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "ano" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "zip" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "ano_tmp" --algo bm --to 65535 -j DROP
iptables -A INPUT -m string --string "custom_cache" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string ".*zip.*|ano.*|config.*|SpeedUp.*|cache.*data.*" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "data" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "unzipmrpcs.data" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "cache" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "SpeedUp" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "mrpcs_a_s.data" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "config" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "ano" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "zip" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "ano_tmp" --algo bm --to 65535 -j DROP
iptables -A OUTPUT -m string --string "custom_cache" --algo bm --to 65535 -j DROP
iptables -w -I INPUT -m string --string "_s.d"  --algo bm -m length --length 1:65535 -j DROP
iptables -A INPUT -s 129.226.1.157 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.247 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.142 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.64 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.37 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.231 -p tcp -j DROP
iptables -A INPUT -s 129.226.3.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.171 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.142 -p tcp -j DROP
iptables -A INPUT -s 129.226.1.157 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.247 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.142 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.64 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.37 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.231 -p tcp -j DROP
iptables -A INPUT -s 129.226.3.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.171 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.142 -p tcp -j DROP
iptables -A INPUT -s 172.67.170.134 -p tcp -j DROP
iptables -A INPUT -s 129.226.1.157 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.247 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.142 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.64 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.37 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.231 -p tcp -j DROP
iptables -A INPUT -s 129.226.3.232 -p tcp -j DROP
iptables -A INPUT -s 101.32.143.171 -p tcp -j DROP
iptables -A INPUT -s 129.226.2.142 -p tcp -j DROP
iptables -A INPUT -s 1
