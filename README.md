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

```

```

Output

```java

```
