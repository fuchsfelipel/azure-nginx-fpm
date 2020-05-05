# azure-nginx-fpm
Repo containing docker container for running PHP7.3-FPM and Nginx Microsoft Azure. Optimized for Prestashop. Support SSH on Azure Web App for Linux

# Configuration & Deployment
1. Change your domain (and admin directory for Prestashop) in the nginx.conf
2. build the image
3. If deploying on Azure Web App make sure to set App Setting WEBSITES_ENABLE_APP_SERVICE_STORAGE to true. Otherwise your data will be erased every reboot.

# Installing Prestashop
This image will create an empty Nginx + PHP7.3-FPM container. To install prestashop download the installation zip from Prestashop's website and unzip it in the /home/site/wwwroot directory. Follow the installation as usual.
Tip: use apt-get update && apt-get install unzip && unzip [PrestaShop_downloaded_file_here.zip, without the brackets XD].