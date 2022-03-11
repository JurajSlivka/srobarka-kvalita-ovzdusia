# srobarka-kvalita-ovzdusia
 

# Základné príkazy v Ubuntu/Debian CLI
<br>ls ---výpis priečinkov v adresári kde sa nachádzame
<br>ls -a ---výpis všetkých priečinkov v adresári kde sa nachádzame
<br>cd .. ---presun o adresár nižšie
<br>cd .../... ---presun do zadaného adresáru
<br>mkdir ---vytvorenie adresáru 
<br>rm ---vymazanie súboru
<br>rm -r ---vymazanie adreáru
<br>nano ---editor textových súborov
<br>copy SRC DEST ---kopírovanie súboru
<br>git clone ---klonovanie git repozitáru
<br> git clone https://github.com/JurajSlivka/srobarka-kvalita-ovzdusia.git

# Príkazy pre rozbehanie/inštaláciu Dockeru
<br>sudo apt upgrade
<br>sudo apt update
<br>sudo apt-get install docker.io ---inštalácia Docker
<br>docker info ---kontrola inštalácie Dockeru (skontrolujeme či beží Client aj Server)
<br>sudo apt-get install docker-compose ---inštalácia Docker Compose

<br>*ak by sa nespustil server tak zadajte 
<br>sudo chmod 666 /var/run/docker.sock

# Porty kam sa pripájame (viditeľné v docker file)
<br>1883 - nešifrované MQTT
<br>1880 - Nodered
<br>3000 - Grafana
<br>8086 - InfluxDB

# Príkazy pre docker
<br>docker-compose up ---spustenie všetkých kontajnerov v docker file
<br>docker container ls ---výpis bežiacich kontajnerov
<br>docker volume ls ---výpis dátových priečinkov dockeru
<br>docker --help

# Setup MQTT 
<br>Priečinok kde sa nachádzajú súbory projektu /var/lib/docker/volumes
<br>Nutné upraviť v mosquitto config file:
<br>listener 1883 ---pridanie portu na ktorý sa pripájame (nezabezpeceny port|
<br>allow_anonymus true ---povolime nesifrovanu komunikaciu
<br>Ďalšie konfiguračne informácie sa nachádzajú v config file

