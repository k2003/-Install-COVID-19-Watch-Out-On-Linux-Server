#Install COVID-19 Watch Out On Linux Server
#CentOS Install Zip Unzip
yum install zip unzip -y
cd /var/www/html
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-full-setup.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-verion2.1.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-2.2.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-2.3.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-2.4.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-2.5.zip
wget http://covid19.cbo.moph.go.th/covid19/downloads/covid-wo-update-2.6.zip
unzip -o covid-wo-full-setup.zip
unzip -o covid-wo-update-verion2.1.zip
unzip -o covid-wo-update-2.2.zip
unzip -o covid-wo-update-2.3.zip
unzip -o covid-wo-update-2.4.zip
unzip -o covid-wo-update-2.5.zip
unzip -o covid-wo-update-2.6.zip
#CHMOD
chcon -R -t httpd_sys_content_rw_t /var/www/html/covid-wo
cd /var/www/html/covid-wo
#ติดตั้งแล้วตั้งค่าการเชื่อต่อฐานข้อมูลที่ covid-wo/includes/conf.ini.php
