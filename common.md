# check port
nc -z サーバ名  ポート番号
telnet [アクセス先IP] [アクセス先ポート]
sudo traceroute -T -p [アクセス先ポート] [アクセス先IP]

## shell snippets
targets=("hosta" "hostb" "hostc")
for t in ${targets[@]}; do
    ssh -t kli@$t "sudo xxx"
done

# screen
## enter screen
screen
## check all screen
screen -ls
## restore screen
screen -r
## create new tab
ctrl-a + c
## move to next tab
ctrl-a + n
## quit screen
ctrl-a + d

sudo tcpdump -Z root -i enp7s0 port 8765
