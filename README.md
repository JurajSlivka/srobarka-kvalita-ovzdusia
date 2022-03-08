# srobarka-kvalita-ovzdusia

#Základné príkazy v Ubuntu/Debian CLI
<br>ls ---výpis priečinkov v adresári kde sa nachádzame
<br>ls -a ---výpis všetkých priečinkov v adresári kde sa nachádzame
<br>cd .. ---presun o adresár nižšie
cd .../... ---presun do zadaného adresáru
mkdir ---vytvorenie adresáru 
rm ---vymazanie súboru
rm -r ---vymazanie adreáru
nano ---editor textových súborov
copy SRC DEST ---kopírovanie súboru
git clone ---klonovanie git repozitáru

# Príkazy pre rozbehanie inštaláciu Dockeru
sudo apt upgrade
sudo apt update
curl -sSL https://get.docker.com/ | sh
docker info
sudo apt get docker-compose

*ak by sa nespustil server tak zadajte 
sudo chmod 666 /var/run/docker.sock

# Porty kam sa pripájame (viditeľné v docker file)
1883 - nešifrované MQTT
1880 - Nodered
3000 - Grafana
8086 - InfluxDB

# Príkazy pre docker
docker-compose up
docker container ls
docker volume ls
docker --help

# Setup MQTT 
Priečinok kde sa nachádzajú súbory projektu /var/lib/docker/volumes
Nutné upraviť v MQTT config file:
listener 1883 ---pridanie portu na ktorý sa pripájame (nezabezpeceny port|
allow_anonymus true ---povolime nesifrovanu komunikaciu
Ďalšie konfiguračne informácie sa nachádzajú v config file

