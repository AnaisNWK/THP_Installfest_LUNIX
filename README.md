# THP_Installfest_LUNIX

### Installation des librairies et packages : 
```
sudo apt-get install autoconf automake bison build-essential curl git-core libapr1 libaprutil1 libc6-dev libltdl-dev libsqlite3-0 libsqlite3-dev libssl-dev libtool libxml2-dev libxslt-dev libxslt1-dev libyaml-dev ncurses-dev nodejs openssl sqlite3 zlib1g zlib1g-dev libreadline7
```
### Git : 
```
sudo apt-get install git
```
Vérifier la version installée :
```
git --version
#=> git version 2.x.x
```

### Configurer son compte GitHub
```
git config --global user.name "Ecris ton nom ici, en gardant les quotes"
```
```
git config --global user.email "Ecris ton email ici, en gardant les quotes"
```
Configurer le SSH 
```
ls ~/.ssh/id_rsa
```
> So le résultat est une erreur : 
> Lancer la commande `ssh-keygen -C ton_email@ton_email.com -t rsa`

### RVM :

> Avant de se lancer dans l'installation de la RVM, vérifier que votre terminal soit bien en mode "login shell"
> => Préférence du terminal > Title and Command > check the box "Run command as a login shell"

```
curl -L get.rvm.io | bash -s stable
```
> Si erreur : `GPG signature verification failed`
> lancer : `ssh-keygen -C ton_email@ton_email.com -t rsa` et suivre les instructions  
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```
(gpg ou gpg2 selon l'erreur)

Pour vérifier si RVM fonctionne : 
```
type rvm | head -1
#=> rvm is a function
```
```
rvm -v
rvm 1.x.x (latest) by Michal Papis, Piotr Kuczynski, Wayne E. Seguin [https://rvm.io]
```
### Ruby
```
rvm install 2.5.1
```
> Si erreur : `autoreconf was not found in the PATH`, lancer `sudo apt-get install automake`puis relancer `rvm install 2.5.1`

```
rvm use 2.5.1
```
```
rvm --default use 2.5.1
```
> On vérifie si c'est bien installé en tapant `ruby -v`

### Rails
```
gem install rails -v 5.2.3
```
> On vérifie si c'est bien installé en tapant `rails -v`


