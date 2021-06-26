1. Required packages

sudo apt-get update
sudo apt-get install openjdk-8-jdk
sudo apt-get install gitweb
sudo apt-get install git-review

2. Link for gerrit and tools
 a. https://gerrit-releases.storage.googleapis.com/index.html
 b. https://gerrit-ci.gerritforge.com
 c. https://groups.google.com/forum/#!topic/repo-discuss/fmHMQpN-qMQ

3. Create gerrit user

sudo useradd gerrit && groupadd gerrit
cd /home
mkdir gerrit
chown -R gerrit:gerrit gerrit

4. Create folders in gerrit

cd /home/gerrit/
mkdir lib && mkdir plugins

5. Setup MySQL
 https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04

6. Setup gerrit MySQL

mysql -p
CREATE USER 'gerrit'@'localhost' IDENTIFIED BY 'yourpassword';
CREATE DATABASE reviewdb;
GRANT ALL ON reviewdb.* TO 'gerrit'@'localhost';
FLUSH PRIVILEGES;
exit;

7. Location for gerrit plugins

/home/gerrit/gerrit*.war
/home/gerrit/lib/github-oauth-2.14-SNAPSHOT.jar
/home/gerrit/plugins/github-plugin-2.14-SNAPSHOT.jar

8. Configure Gerrit

cd /home/gerrit
sudo java -jar gerrit*.war init
sudo java -jar gerrit*.war reindex
cd /home/
sudo chown -R gerrit:gerrit gerrit


http://firelord.me/assets/images/gerrit/Screenshot%20(9).png
http://firelord.me/assets/images/gerrit/Screenshot%20(10).png


