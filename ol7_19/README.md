# Oracle Database 19c on Docker

The following article provides a description of this Dockerfile -> [Docker : Oracle Database 19c](https://reybis.com/posts/oracle-database-19c-docker)

- [Oracle Database 19c on Docker](#oracle-database-19c-on-docker)
	- [Software](#software)
	- [Directory structure](#directory-structure)
	- [Persistent Storage](#persistent-storage)
	- [How to use](#how-to-use)
			- [Build the image](#build-the-image)
			- [Run - Non-persistent storage](#run-non-persistent-storage)
			- [Run - Persistent storage](#run-persistent-storage)
			- [Container Logs](#container-logs)
			- [Execute bash shell](#execute-bash-shells)
			- [Start the container](#start-the-container)
			- [Stop the container](#stop-the-container)
			- [Remove the container](#remove-the-container)
	- [Credits](#credits)
  - [Changelog](#changelog)

## Software 
Due to licensing restrictions I can't host these files in Github or elsewhere. 

As such, you'll need to download them manually. Download the following files and store them in the `software` folder.
- [apex_20.1.zip](https://www.oracle.com/technetwork/developer-tools/apex/downloads/index.html)
- [LINUX.X64_193000_db_home.zip](https://www.oracle.com/technetwork/database/enterprise-edition/downloads/index.html)

## Directory structure
Directory contents when software is included.

```
.
├── Dockerfile
├── README.md
├── scripts
│   ├── healthcheck.sh
│   └── start.sh
└── software
    ├── apex_20.1.zip
    ├── LINUX.X64_193000_db_home.zip
    └── put_software_here.txt
```

## Persistent Storage
The data volume to use for the ORDS/Tomcat server `/u02`. If omitted the ORDS/Tomcat installation will not be persisted over container recreation.

Use with docker run ` -v [<host mount point>:]/u02`

If you are using an external host volume for persistent storage, the build expects it to owned by a group with the group ID of 1042. This is described here.

[Docker : Host File System Permissions for Container Persistent Host Volumes](https://oracle-base.com/articles/linux/docker-host-file-system-permissions-for-container-persistent-host-volumes)


## How to use

### Build the image
```
docker build -t ol7_19:latest .
```

```
docker build --squash -t ol7_19:latest .
```

### Run - Non-persistent storage
```
docker run -dit --name ol7_19_con -p 1521:1521 -p 5500:5500 --shm-size="1G" ol7_19:latest
```

### Run - Persistent storage
```
docker run -dit --name ol7_19_con -p 1521:1521 -p 5500:5500 --shm-size="1G" -v /u01/volumes/ol7_19_con_u02/:/u02 ol7_19:latest
```

Persistent storage and part of Docker network called "oracle_network".
```
docker run -dit --name ol7_19_con -p 1521:1521 -p 5500:5500 --shm-size="1G" --network=oracle_network -v /u01/volumes/ol7_19_con_u02/:/u02 ol7_19:latest
```

### Container Logs
```
docker logs --follow ol7_19_con
```

### Execute bash shell
```
docker exec -it ol7_19_con bash
```

### Stop the container
```
docker stop --time=30 ol7_19_con
```

### Start the container
```
docker start ol7_19_con
```

### Remove the container
```
docker rm -vf ol7_19_con 
```

## Credits
Oracle-base docker files by [Tim Hall](https://github.com/oraclebase/dockerfiles)

## Changelog

#### 1.0.0 - Initial Release