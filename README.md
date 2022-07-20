# weather-canada-telegraf-influxdb-grafana

# 🚀 Reads WeatherCanada atom feeds to ingest into influxdb with telegraf and grafana 🚀

https://github.com/coding-to-music/weather-canada-telegraf-influxdb-grafana

From / By Nathan Beals https://github.com/ndbeals

https://github.com/ndbeals/weathercanada-influxdb

## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/weather-canada-telegraf-influxdb-grafana.git
git push -u origin main
```

## docker-compose up

```java
docker-compose up
```

Output:

```java

```

## docker-compose down

```
docker-compose down
```

Output

```java
Stopping weathercan-python ... done
Stopping hddtemp           ... done
Removing speedtest         ... done
Removing weathercan-python ... done
Removing influxdb          ... done
Removing grafana           ... done
Removing chronograf        ... done
Removing hddtemp           ... done
Removing network weather-canada-telegraf-influxdb-grafana_default
```

## checking ports and who uses them

https://linuxhandbook.com/check-open-ports-linux/

```
sudo netstat -nlp
```

```java
sudo lsof -i

sudo lsof -i -P -n

sudo lsof -i -P -n | grep LISTEN

nc -z -v <IP-ADDRESS> 1-65535 2>&1 | grep -v 'Connection refused'

sudo netstat -lptu

sudo netstat -tulpn

nc -z -v <IP-ADDRESS> 1-65535 2>&1 | grep -v 'Connection refused'

```

## Docker commands

```
docker-compose up
docker-compose down

docker ps

docker volume ls
```

## errors from docker-compose up

```
docker-compose up
```

Output

```
Creating network "weather-canada-telegraf-influxdb-grafana_default" with the default driver
Creating hddtemp ...
Creating chronograf ...
Creating grafana    ...
Creating influxdb   ...
Creating influxdb          ... error
Creating weathercan-python ...
Creating chronograf        ... error

ERROR: for influxdb  Cannot start service influxdb: driver failed programming external connectivity on endpoint influxdb (56245f40540940d6e6b39e3a231d58683b218392b3a842b823bb1bc963d8cdd5): Error starting userland proxy: listen tcp4 :8086: bind: cannot assign requested address
WARNING: Host is already in use by another container
Creating grafana           ... error
ERROR: for chronograf  Cannot start service chronograf: driver failed programming external connectivity on endpoint chronograf (1a9f170a71d0a19eec15df6df07f55c60817f0de9b8bab47c5e248ebcd978cd5): Error starting userland proxy: listen tcp4 :8087: bind: cannot assign requested address
WARNING: Host is already in use by another container

Creating hddtemp           ... done requested address

ERROR: for speedtest  Cannot start service speedtest: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: error during container init: error mounting "//weather-canada-telegraf-influxdb-grafana/config.ini" to rootfs at "/src/config.ini": mount /config.ini:/src/config.ini (via /proc/self/fd/6), flags: 0x5000: not a directory: unknown: Are you trying to mount a directory onto a file (or vice-versa
Creating weathercan-python ... done

ERROR: for influxdb  Cannot start service influxdb: driver failed programming external connectivity on endpoint influxdb (56245f40540940d6e6b39e3a231d58683b218392b3a842b823bb1bc963d8cdd5): Error starting userland proxy: listen tcp4 :8086: bind: cannot assign requested address

ERROR: for chronograf  Cannot start service chronograf: driver failed programming external connectivity on endpoint chronograf (1a9f170a71d0a19eec15df6df07f55c60817f0de9b8bab47c5e248ebcd978cd5): Error starting userland proxy: listen tcp4 :8087: bind: cannot assign requested address

ERROR: for grafana  Cannot start service grafana: driver failed programming external connectivity on endpoint grafana (81e78c570a39362f79012d1ad79b9f07b86756e47248f1bb6e006d680a8e18cf): Error starting userland proxy: listen tcp4 :3001: bind: cannot assign requested address

ERROR: for speedtest  Cannot start service speedtest: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: error during container init: error mounting "/config.ini" to rootfs at "/src/config.ini": mount /config.ini:/src/config.ini (via /proc/self/fd/6), flags: 0x5000: not a directory: unknown: Are you trying to mount a directory onto a file (or vice-versa)? Check if the specified host path exists and is the expected type
ERROR: Encountered errors while bringing up the project.
```
