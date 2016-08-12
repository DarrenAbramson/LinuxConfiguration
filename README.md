# LinuxConfiguration

This describes the steps taken to deploy my project for the Udacity Full Stack Development nanodegree to a provided AWS EC2 instance.

IP address of server: 	`http://52.42.254.155/`
SSH port of server:		`2200`

NOTE: much of the steps taken were modified from [this page](https://github.com/elnobun/Linux-Server-Configuration) linked from the Udacity forum for P7.

Steps taken:

```
nano /etc/hosts
sudo -v
sudo adduser grader
visudo
su - grader
date -u
nano /etc/ssh/sshd_config
sudo service ssh restart
exit
su - grader
sudo ufw default deny incoming
sudo ufw allow 2200/tcp
sudo ufw allow 80/tcp
sudo ufw allow 123/udp
sudo ufw enable
exit
sudo dpkg-reconfigure tzdata
sudo apt-get install apache2
sudo apt-get install libapache2-mod-wsgi
nano /etc/apache/sites-enabled/000-default.conf
nano /etc/apache2/sites-enabled/000-default.conf
sudo apache2ctl restart
sudo nano /var/www/html/myapp.wsgi
sudo apt-get install postgresql
sudo nano /etc/postgresql/9.1/main/pg_hba.conf
sudo nano /etc/postgresql/9.3/main/pg_hba.conf
cd
ls
pwd
sudo apt-get install git
ls
cd home
ls
cd ~
ls
git clone https://github.com/DarrenAbramson/ItemCatalog.git
ls
cd ItemCatalog
ls
sudo a2enmod wsgi
cd /var/www
ls
cd html
ls
cd ..
ls
mkdir Catalog
ls
cd catalog
ls
mkdir static templates
ls
nano __init__.py
sudo apt-get install libapache2-mod-wsgi python-dev
ls
nano __init.py__
cd ..
ls
cd ..
ls
cd Catalog
ls
cd catalog
ls
nano __init__.py
sudo apt-get install python-pip
sudo pip install virtualenv
sudo virtualenv venv
/var/www/Catalog/catalog$ source venv/bin/activate
cd ..
/var/www/Catalog/catalog$ source venv/bin/activate
pwd
/var/www/Catalog/catalog$ source venv/bin/activate
cd Catalog/catalog
ls
/var/www/Catalog/catalog$ source venv/bin/activate
/var/www/Catalog/catalog/ source venv/bin/activate
/var/www/Catalog/catalog source venv/bin/activate
/var/www/Catalog/catalog$ source venv/bin/activate
ls
source venv/bin/activate
pip install Flask
python __init.py__
ls
python __init__.py
deactivate
sudo nano /etc/apache2/sites-available/catalog.conf
sudo a2ensite catalog.wsgi
ls
cd /var/www/Catalog
ls
sudo nano catalog.wsgi
sudo service apache2 restart
git clone #!/user/bin/python
import sys
import logging
logging.basicConfig(stream=sys.stderr)
sys.path.insert(0,"/var/www/Catalog/catalog/")
from catalog import app as application
git clone https://github.com/DarrenAbramson/ItemCatalog.git
ls
mv ItemCatalog/* catalog/
ls
cd catalog
ls
cd ..
ls
sudo nano .htaccess
ls
cd catalog
source venv/bin/activate
sudp apt-get install python-setuptools
sudo apt-get install python-setuptools
sudo pip install Flask
pip install httplib2
pip install requests
sudo pip install flask-seasurf
apt-get install python-psycopg2
pip install sqlalchemy
sudo apache2ctl restart
nano database_setup.py
```

