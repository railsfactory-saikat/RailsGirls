
# Steps to install rails, rvm ruby, postgres 

```sh
$ sudo apt-get update
$ sudo apt-get install build-essential
$ sudo apt-get install curl

$ gpg --keyserver hkp://keys.gnupg.net --recv-keys
409B6B1796C275462A1703113804BB82D39DC0E3
7D2BAF1CF37B13E2069D6956105BD0E739499BDB

```

# RVM installation
```sh
$ \curl -sSL https://get.rvm.io | bash -s stable
$ source ~/.rvm/scripts/rvm
```
copy paste the suggested path here, change terminal profile preferences
Open ternimal --> Edit --> Profile Preferences --> check (run command as login shell)
```sh
$ rvm
```
Shows all commands of rvm
```sh
$ rvm install 2.5.3
$ rvm use 2.5.3 –default
```
To set a default version
```sh
$ ruby -v
```
To check installed current ruby version
```sh
$ rvm list
```
To check installed ruby versions Rails installation
```sh
$ gem install rails
```
# Possible error
Can't find gem railties (>= 0.a) with executable rails
(Gem::GemNotFoundException)
Then follow
```s
$ gem install rails
$ gem install rails --version=5.2.2.0
$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
$ sudo apt-get install -y build-essential
```
# Creating a New Rails Project
```s
$ rails new app_name –database=postgresql
cd app_name
rails s #to start server 
```
# pgAdmin

goto APP in ubuntu search for pgadmin install and launch

Postgres installation

$ sudo apt-get update

$ sudo apt-get install postgresql-10

$ sudo vi /etc/postgresql/10/main/postgresql.conf

## any error here do replace the file in respective file with attatched file in same path
```sh
$ sudo systemctl restart postgresql.service

$ sudo -i -u postgres

$ createuser –interactive
```
# Open pgAdmin, to connect... provide
name --> any_name
host   --> localhost
password --> root
 # To check the installed version of postgres if properly installed
```sh
$ psql -V  
```  



# database.yml  file configuration

```s
*** maintain indentation ***
default: &default
 adapter: postgresql
 encoding: utf8
 timeout: 500
 pool: 5
 username: postgres
 password: root
 host: localhost

development: 
 <<: *default
 database: sample
```




