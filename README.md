i installed a new ubuntu server and cloned the server. I named the new server Nike Ubuntu prefix.

I installed Lamp server on the original ubuntu server using the following steps.

I changed the 'user permission to root using ' sudo -i  then i updated my system using 'apt-get update 
I proceeded to installing lamp server using 'apt-get install lamp-server^
I was asked to create a strong password which i did then i chose y/n to continue. I chose y
The next step was to start the wordpress database initilization with'mysql-u root -p'
i moved on to creating username and password for wordpress then i took the following steps
 GRANT PRIVILEGES ON wordpressdb.* TO wordpressuser@localhost;
FLUSH PRIVILEGES and
EXIT

I moved on to temporary folder'cd /tmp
i installed wordpress using ' wget http://wordpress.org/latest.zip
i moved on to unzip using 'unzip -q latest.zip -d /var/www/html/wordpress then i put the following commands so wordpress can be installed properly
chown -R www-data:www-data /var/www/html/wordpress
chmod -R 755 /var/www/html/wordpress
mkdir -p /var/www/html/wordpress/wp-content/uploads
chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads

The next step was to get the ip address of my server using 'ifconfig' then i opened the wordpress configuration page.
i used localhost/wordpress. 
I was asked for the database name, username, password and datahost host to set it up. I set up the site name, password and email. 
I was able to get into wordpress dashboard.
