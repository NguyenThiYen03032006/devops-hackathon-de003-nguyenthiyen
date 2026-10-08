## 1. Thông tin sinh viên
- Nguyễn Thị Yến
- PTIT-HN-158
- CNTT2
- nguyenthiyen-k24cntt2
- Github: devops-hackathon-de003-nguyenthiyen
## Môi trường
sudo apt update && sudo apt install -y nginx git ufw curl

# Bật và khởi động Nginx
sudo systemctl enable nginx
sudo systemctl start nginx

# Cấu hình Git
git config --global user.name "nguyenthiyen03032006"
git config --global user.email "nguyenthiyen03032006@example.com"

##Nginx
nguyenthiyen-k24cntt2@VM02:~$ sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
nguyenthiyen-k24cntt2@VM02:~$ sudo systemctl is-active --now nginx
active
nguyenthiyen-k24cntt2@VM02:~$  sudo systemctl enable --now nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable nginx
## Tường lửa
nguyenthiyen-k24cntt2@VM02:~$ sudo ufw allow 22/tcp
Rules updated
Rules updated (v6)
nguyenthiyen-k24cntt2@VM02:~$ sudo ufw allow 8082/tcp
Rules updated
Rules updated (v6)
nguyenthiyen-k24cntt2@VM02:~$ sudo ufw --force enable
Firewall is active and enabled on system startup
nguyenthiyen-k24cntt2@VM02:~$ sudo ufw status verbose
Status: active
Logging: on (low)
Default: deny (incoming), allow (outgoing), disabled (routed)
New profiles: skip

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW IN    Anywhere
8082/tcp                   ALLOW IN    Anywhere
22/tcp (v6)                ALLOW IN    Anywhere (v6)
8082/tcp (v6)              ALLOW IN    Anywhere (v6)
