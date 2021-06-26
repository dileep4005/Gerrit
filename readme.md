Using secure store: com.google.gerrit.server.securestore.DefaultSecureStore
[2016-05-04 18:38:32,750] [main] INFO  com.google.gerrit.server.config.GerritServerConfigProvider : No /home/gerrit/./etc/gerrit.config; assuming defaults

*** Gerrit Code Review 2.12.2
*** 


*** Git Repositories
*** 

Location of Git repositories   [git]: 

*** SQL Database
*** 

Database server type           [h2]: mysql
Gerrit Code Review is not shipped with MySQL Connector/J 5.x
**  This library is required for your configuration. **
Download and install it now [Y/n]?
Downloading http://repo2.maven.org/maven2/mysql/mysql-connector-java/5.x/mysql-connector-java-5.x.jar ... OK
Checksum mysql-connector-java-5.1.10.jar OK
Server hostname                [localhost]: 
Server port                    [(mysql default)]: 
Database name                  [reviewdb]: 
Database username              [root]: gerrit
gerrit's password              : 
              confirm password : 

*** Index
*** 

Type                           [LUCENE/?]: 

The index must be rebuilt before starting Gerrit:
  java -jar gerrit.war reindex -d site_path

*** User Authentication
*** 

Authentication method          [OPENID/?]: http
Get username from custom HTTP header [y/N]? y
Username HTTP header           [SM_USER]: GITHUB_USER
SSO logout URL                 : 
Enable signed push support     [y/N]? 

*** Review Labels
*** 

Install Verified label         [y/N]? 

*** Email Delivery
*** 

SMTP server hostname           [localhost]: smtp.gmail.com
SMTP server port               [(default)]: 587
SMTP encryption                [NONE/?]: TLS
SMTP username                  [root]: aexgerrit@gmail.com
aexgerrit@gmail.com's password : 
              confirm password : 

*** Container Process
*** 

Run as                         [root]: gerrit
Java runtime                   [/usr/lib/jvm/java-7-openjdk-amd64/jre]: 
Copy gerrit-2.12.2.war to ./bin/gerrit.war [Y/n]? 
Copying gerrit-2.12.2.war to ./bin/gerrit.war

*** SSH Daemon
*** 

Listen on address[*]: 
Listen on port                 [29418]: 

Gerrit Code Review is not shipped with Bouncy Castle Crypto SSL v152
  If available, Gerrit can take advantage of features
  in the library, but will also function without it.
Download and install it now [Y/n]? n
Generating SSH host key ... rsa(simple)... done

*** HTTP Daemon
*** 

Behind reverse proxy           [y/N]? 
Use SSL (https://)             [y/N]? 
Listen on address[*]: 
Listen on port                 [8080]: 
Canonical URL                  [http://aex-gerrit:80/]: http://gerrit.aospextended.com     

*** Plugins
*** 

Installing plugins.
Install plugin singleusergroup version v2.12.2 [y/N]? y
Install plugin commit-message-length-validator version v2.12.2 [y/N]? y
Install plugin reviewnotes version v2.12.2 [y/N]? y
Install plugin replication version v2.12.2 [y/N]? y
Install plugin download-commands version v2.12.2 [y/N]? y
Initializing plugins.

*** GitHub Integration
*** 

GitHub URL                     [https://github.com]: 
GitHub API URL                 [https://api.github.com]: 

NOTE: You might need to configure a proxy using http.proxy if you run Gerrit behind a firewall.

*** GitHub OAuth registration and credentials
*** 

Register Gerrit as GitHub application on:
https://github.com/settings/applications/new

Settings (assumed Gerrit URL: http://gerrit.aospextended.org/)
* Application name: Gerrit Code Review
* Homepage URL: http://gerrit.aospextended.com/
* Authorization callback URL: http://gerrit.aospextended.com/oauth

After registration is complete, enter the generated OAuth credentials:
GitHub Client ID               :  (ENTER THE APPLICATION CLIENT ID)
GitHub Client Secret           :  (ENTER THE APPLICATION CLIENT SECRET)
              confirm password :  (REENTER THE APPLICATION CLIENT SECRET)
Gerrit OAuth implementation    [HTTP/?]: http
HTTP Authentication Header     [GITHUB_USER]: 

Initialized /home/gerrit
