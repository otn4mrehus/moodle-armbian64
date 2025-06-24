# moodle-armbian64
Moodle on Armbian 64
### Download 
```
mkdir -p ~/docker && cd ~/docker && \
git clone https://github.com/otnamrehus/moodle-armbian64.git && \
cd moodle-armbian64 && \
mkdir -p mariadb_data/ moodledata/ moodle/ && \ 
chmod -R 775 mariadb_data/ moodledata/ moodle/ 
```
### Clean Direktori
```
rm -R mariadb_data/ moodle/  moodledata/ && \
chmod -R 775 mariadb_data/ moodledata/ moodle/
```
### Run Docker
```
docker-compose -f "docker-compose_MOODLE_5.0-MARIADB_11.2.yaml" -p 'moodle' up --build
```
### Remove Docker
```
docker-compose -f "docker-compose_MOODLE_5.0-MARIADB_11.2.yaml" -p 'moodle' down -v
```
### Start | Stop Container
```
docker-compose -f "docker-compose_MOODLE_5.0-MARIADB_11.2.yaml" -p 'moodle' start | stop | restart
```
