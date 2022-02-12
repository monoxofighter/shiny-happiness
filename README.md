# shiny-happiness

# Part 01
```
apt-get update -y; apt-get upgrade -y; sudo wget https://raw.githubusercontent.com/monoxofighter/shiny-happiness/master/part1; chmod 777 part1; ./part1
```
# Install Cetificates 

```
sudo certbot certonly --standalone --preferred-challenges http --agree-tos --email (cloudflara email) -d (you domain)
```
# Part 02

```
apt-get update -y; apt-get upgrade -y; sudo wget https://raw.githubusercontent.com/monoxofighter/shiny-happiness/master/part2; chmod 777 part2; ./part2
```
# With Open All Ports 
```
apt-get update -y; apt-get upgrade -y; sudo wget https://raw.githubusercontent.com/monoxofighter/shiny-happiness/main/allports; chmod 777 allports; ./allports
```
# Setup Automatic Reboot @ Every day 5 a.m.
```
(crontab -l && echo "0 5 * * * /sbin/reboot") | crontab -
```
# Check current expiry date
```
openssl x509 -noout -dates -in /etc/letsencrypt/live/yourdomain.com/cert.pem
```
replace "yourdomain.com" with your doamin.

# SSL Auto Renew - Method 1 (complex)
```
apt-get update -y; apt-get upgrade -y; sudo wget https://raw.githubusercontent.com/monoxofighter/shiny-happiness/master/autorenewssl; chmod 777 autorenewssl; ./autorenewssl
```
# SSL Auto Renew - Method 2 (easy)
```
sudo crontab -e
```
if you're using this 1st time select nano , choosing number 1
and enter this line in to editor 
```
0 6 * * 0 certbot renew -n -q --pre-hook "sudo x-ui stop" --post-hook "sudo x-ui start"
```
after that press ctrl+x > y > Enter

# Features
01.Firewall Settings

02.Speedtest Install

03.Setup Time Zone

04.Remove Junk Files (Automated)

05.Install SSL

06.Cronjabs for SSL Auto Renew

07.Auto Start Cronjob
