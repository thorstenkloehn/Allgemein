---
title: "Installieren"
date: 2023-12-07T19:00:31+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Installieren"
    weight: 0.5
    
---
# Ubuntu installieren
## Voraussetzungen

- [x] Ubuntu 18.04 LTS oder höher
- [x] Root Zugriff
- [x] SSH Zugriff
- [x] Internet Verbindung

## Ubuntu 18.04 LTS oder höher
Browser öffnen und auf [Ubuntu](https://ubuntu.com/download/desktop) gehen und die gewünschte Version herunterladen.
### usb-stick erstellen
#### Windows
- [x] [Rufus](https://rufus.ie/) herunterladen
- [x] Rufus starten
- [x] USB-Stick auswählen
- [x] ISO-Image auswählen
- [x] Starten
#### Ubuntu Deskop
-  USB-Stick einstecken
- Programm Startmedienerstellen öffnen
- ISO-Image auswählen
- USB-Stick auswählen
- Starten

### Ubuntu installieren

- USB-Stick einstecken
- PC neustarten
- Bootmenü öffnen
- USB-Stick auswählen
- Ubuntu installieren
- Sprache auswählen
- Tastatur auswählen
- Installationstyp auswählen
- Benutzerdaten eingeben
- Installation starten
-  Neustarten

## ubunru

## Root Zugriff
### Root aktivieren
- Terminal öffnen
- sudo passwd root 
- Passwort eingeben
- Passwort wiederholen
- Neustarten
### Root anmelden
- Terminal öffnen
- `su` eingeben
- Passwort eingeben
## Vorbereitung

### Aktualisieren

- Öffne Sie das Terminal und auf ihrem Ubuntu-Desktop
- Führen Sie folgenden Befehl aus,um System zu aktualisieren.
```bash
sudo apt-get update 
sudo apt-get upgrade
```
### Google Chrome Installieren
firefox starten und folgende Seite öffnen
- [Download Google Chrome](https://www.google.com/intl/de_de/chrome/)
- Klicken Sie auf Download Chrome.
- Klicken Sie auf Akzeptieren und installieren.

```bash
 sudo dpkg -i google-chrome-stable_current_amd64.deb
 ```
- Klicken Sie auf Ausführen oder Speichern.
- Wenn Sie auf Speichern geklickt haben, doppelklicken Sie auf die Download-Datei.
- Starten Sie Chrome:
- Ubuntu: Ein Fenster wird angezeigt, in dem Sie auf Chrome öffnen      klicken können.
- Wenn Sie aufgefordert werden, dass Chrome Standardbrowser wird oder ob Sie Benachrichtigungen von Chrome erhalten möchten, wählen Sie Ja aus.
- Fertig! Chrome ist auf Ihrem Desktop und in Ihrem Anwendungs-Menü verfügbar.


#### Ubuntu 20.04 Lts gh installieren
```bash
type -p curl >/dev/null || (sudo apt update && sudo apt install curl -y)
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg \
&& sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```
##### Webadresse ist
- [Download gh](https://cli.github.com/)

### Git Installieren
```bash
sudo apt-get install git  gh
git config --global user.email "you@example.com"
git config --global user.name "Your Name"

```
#### gh Konfigurieren

```bash
gh auth login
```
### Programmiersprachen Installieren

#### Rust Installieren
```bash
sudo apt  install curl 
sudo apt install build-essential
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
#### Nodejs Installieren
* [Nodejs Installieren](https://github.com/nodesource/distributions/blob/master/README.md)

#### Go Installieren
```bash
wget https://golang.org/dl/go1.21.5.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.21.5.linux-amd64.tar.gz

sudo nano ~/.bashrc
```
#### Go Umgebungsvariablen setzen
```bash
export PATH=$PATH:/usr/local/go/bin
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```
#### Go Umgebungsvariablen setzen
```bash
source ~/.bashrc
```
## Java Installieren
```bash
sudo apt install openjdk-21-jdk
```
## Visual Studio Code 
### Installieren
```bash
sudo snap install code --classic
```
### Pflugin
```bash 
code .
```
- Starten Sie VS Code Quick Open ( Ctrl+P), fügen Sie den folgenden Befehl ein und drücken Sie die Eingabetaste.
```bash
code --install-extension GitHub.copilot
code --install-extension MS-CEINTL.vscode-language-pack-de
code --install-extension rust-lang.rust-analyzer
code --install-extension eliostruyf.vscode-hugo-themer
code --install-extension ckolkman.vscode-postgres
code --install-extension formulahendry.code-runner
code --install-extension vscjava.vscode-java-pack
```
## Hugo
- Installieren Sie Hugo mit folgendem Befehl.
```bash
sudo snap install hugo
```
- Erstellen Sie ein neues Projekt mit folgendem Befehl.
```bash
hugo new site Hugo
```
- Wechseln Sie in das Verzeichnis mit folgendem Befehl.
```bash
cd Hugo
```
### Weblinks
- [Hugo](https://gohugo.io/)

 ## Datenbank
### PostgreSQL
#### Installation

```bash
sudo apt-get install postgresql-all
```
### PosgreSQL Version zeigen
```bash
psql --version
```

### Postgis Installation in Ubuntu 23.04
```bash
sudo apt install postgis postgresql-16-postgis-3 postgresql-16-postgis-3-scripts
```
### Installation von osm2pgsql
```bash
sudo apt-get install osm2pgsql
```

### Datenbank erstellen
```bash
## Neuen Benutzer anlegen
sudo adduser thorsten
sudo usermod -aG sudo thorsten

## Benutzer thorsten zu Gruppe postgres hinzufügen


sudo -u postgres -i
createuser thorsten
createdb -E UTF8 -O thorsten thorsten
psql
\c thorsten
CREATE EXTENSION postgis;
CREATE EXTENSION hstore;
ALTER TABLE geometry_columns OWNER TO thorsten;
ALTER TABLE spatial_ref_sys OWNER TO thorsten;
\q
exit
## Passwort für den Benutzer postgres setzen
\password thorsten
\q
exit

```
### Datenbank mit osm2pgsql befüllen
```bash
wget https://download.geofabrik.de/europe/germany/schleswig-holstein-latest.osm.pbf
osm2pgsql  -d thorsten --create  -G --hstore  schleswig-holstein-latest.osm.pbf
```


### Datenbank Löschen
```bash
sudo -u postgres -i
psql
GRANT ALL PRIVILEGES ON DATABASE thorsten TO postgres;
drop database thorsten;
\q
```
## Was ist Nginx?
Nginx ist ein Webserver, der sich durch seine hohe Performance auszeichnet. Er ist für viele Betriebssysteme verfügbar und kann als Reverse Proxy, Load Balancer, Mail Proxy und HTTP Cache verwendet werden. Nginx ist Open Source und wird unter der BSD-Lizenz veröffentlicht.

### Installation Nginx

*  [Nginx Installieren](https://nginx.org/en/linux_packages.html#Ubuntu/) 
```bash
sudo apt install nginx
nginx -v # Version anzeigen

```
### Website Installieren
```bash
git clone https://github.com/thorstenkloehn/ahrensburg.city.git
git clone https://github.com/thorstenkloehn/Allgemein.git

```
#### cerbort Installation
```bash
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
```

#### Zertifikat erstellen
```bash
sudo rm /etc/nginx/sites-enabled/default
sudo systemctl stop nginx
sudo certbot certonly --standalone -d ahrensburg.city -d www.ahrensburg.city
sudo certbot certonly --standalone -d dev.ahrensburg.city

```

#### Nginx Konfiguration
```bash
sudo nano /etc/nginx/conf.d/ahrensburg.conf
```
#### Nginx Konfiguration
```nginx
server {
    listen 80 default_server;
    listen [::]:80 default_server;

    server_name ahrensburg.city;

    location / {
        return 301 https://$host$request_uri;
    }
}

server {
    listen 443 ssl http2;
    listen [::]:443 ssl http2;
    server_name ahrensburg.city;
    ssl_certificate /etc/letsencrypt/live/ahrensburg.city/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/ahrensburg.city/privkey.pem;
    root /home/thorsten/ahrensburg.city/public;

    location / {
        try_files $uri $uri/ =404;
    }
}

server {
    listen 443 ssl http2;
    listen [::]:443 ssl http2;
    server_name dev.ahrensburg.city;
    ssl_certificate /etc/letsencrypt/live/dev.ahrensburg.city/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/dev.ahrensburg.city/privkey.pem;
    root /home/thorsten/Allgemein/public;

    location / {
        try_files $uri $uri/ =404;
    }
}

```
## Anki
Anki ist ein Programm zum Lernen von Vokabeln und anderen Inhalten. Es ist für Windows, Linux und Mac OS X verfügbar. Anki ist Open Source und kostenlos. Es ist auch für Android und iOS verfügbar, aber diese Versionen sind nicht kostenlos.

### Anforderungen
```bash
sudo apt install libxcb-xinerama0 libxcb-cursor0
QT_DEBUG_PLUGINS=1 anki

```
### Anki herunterladen
```bash
wget https://github.com/ankitects/anki/releases/download/2.1.66/anki-2.1.66-linux-qt6.tar.zst
```
### Anki installieren
```bash
tar xaf anki-2.1.66-linux-qt6.tar.zst
cd anki-2.1.66-linux-qt6
sudo ./install.sh
```

### Erweiterungen

#### Erweiterungen installieren
```bash
1436550454 1933645497 1463041493 1190756458
```












