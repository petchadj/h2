# H2 database
A H2 Docker images build on official Java 7.

## Usage
Download the image:
```
docker pull petchadj/h2
```

Run as a daemon ('-d' option), exposing ports 1521 (TCP database server) and 81 (web interface). To persist the db data, you need to map the DATA_DIR to a folder on your host ('-v' option):
```
docker run --name=h2 -d -p 1521:1521 -p 81:81 -v /path/to/local/data_dir:/opt/h2-data petchadj/h2
```

Printing logs:
```
docker logs -f h2-log
```
