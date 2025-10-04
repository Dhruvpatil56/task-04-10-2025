Web hosting on Nginx and Apache Tomcat

## NGINX

- Install nginx:
 sudo apt update
 sudo apt install nginx -y

- Place webpage:
 sudo vim /var/www/html/index.html

(p.s - You can add any info in index.html )

- Check service status
 sudo systemctl status nginx

- Restat Nginx
 sudo systemctl restart nginx

- Make sure to update security group with port number 80 allow all traffic 

- Access :http:// <ec2-ip>


##

- Install Apache Tomcat:
 sudo apt update
 sudo apt install tomcat10 tomcat10-admin -y

- Place webpage:
 sudo vim /var/lib/tomcat10/webapps/ROOT/index.html

(p.s - You can add any info in index.html )

- Check service status
 sudo systemctl status tomcat10

- Restat Tomcat
 sudo systemctl restart tomcat

- Make sure to update security group with port number 8080 allow all traffic

- Access :http:// <ec2-ip>:8080


##

I won't be able to host these pages with domain name as currently i don't have any domain name register.

How to host webpages through Route53:

- Register a domain directly from Route53

- Create a DNS record
-> add A record and Cname

- configure nginx conf file add domain-name and www.mydomain.com 

- Enable HTTPS with let's encrypt
    sudo apt install certbot python3-certbot-nginx
    sudo certbot --nginx -d your_domain -d www.your_domain
##
