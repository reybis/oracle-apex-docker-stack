# Oracle REST Data Services (ORDS) 20 on Docker

The following article provides a description of this Dockerfile -> [Docker : Oracle REST Data Services (ORDS)](https://reybis.com/posts/oracle-rest-data-services-ords-docker)

- [Oracle REST Data Services on Docker](#oracle-rest-data-services-(ORDS)-20-on-docker)
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
- [apex_20.1.zip](http://www.oracle.com/technetwork/developer-tools/apex/downloads/index.html)
- [apache-tomcat-9.0.37.tar.gz](https://tomcat.apache.org/download-90.cgi)
- [OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz](https://adoptopenjdk.net/releases.html?variant=openjdk11&jvmVariant=hotspot)
- [ords-20.2.0.178.1804.zip](http://www.oracle.com/technetwork/developer-tools/rest-data-services/downloads/index.html)
- [sqlcl-20.2.0.174.1557.zip](http://www.oracle.com/technetwork/developer-tools/sqlcl/downloads/index.html)

## Directory structure
Directory contents when software is included.

```
.
├── Dockerfile
├── README.md
├── scripts
│   ├── healthcheck.sh
│   ├── install_os_packages.sh
│   ├── ords_software_installation.sh
│   ├── server.xml
│   └── start.sh
└── software
    ├── apache-tomcat-9.0.37.tar.gz
    ├── apex_20.1.zip
    ├── OpenJDK11U-jdk_x64_linux_hotspot_11.0.8_10.tar.gz
    ├── ords-20.2.0.178.1804.zip
    ├── put_software_here.txt
    └── sqlcl-20.2.0.174.1557.zip
```

## Persistent Storage
The data volume to use for the ORDS/Tomcat server `/u01/config/instance1`. If omitted the ORDS/Tomcat installation will not be persisted over container recreation.

Use with docker run ` -v [<host mount point>:]/u01/config/instance1`

If you are using an external host volume for persistent storage, the build expects it to owned by a group with the group ID of 1042. This is described here.

[Docker : Host File System Permissions for Container Persistent Host Volumes](https://oracle-base.com/articles/linux/docker-host-file-system-permissions-for-container-persistent-host-volumes)

## How to use.
Example build and run. Assumes Docker network called "oracle_network" to connect to DB.

### Build the image

```
docker build -t ol7_ords:latest .
```

```
docker build --squash -t ol7_ords:latest .
```

### Run - Non-persistent storage
```
docker run -dit --name ol7_ords_con -p 8080:8080 -p 8443:8443 --network=oracle_network -e DB_HOSTNAME=ol7_183_con ol7_ords:latest
```

### Run - Persistent storage
```
docker run -dit --name ol7_ords_con -p 8080:8080 -p 8443:8443 --network=oracle_network -e DB_HOSTNAME=ol7_183_con -v /home/docker_user/volumes/ol7_183_ords_tomcat:/u01/config/instance1 ol7_ords:latest
```

### Container Logs
```
docker logs --follow ol7_ords_con
```

### Execute bash shell
```
docker exec -it ol7_ords_con bash
```

### Stop the container
```
docker stop --time=30 ol7_ords_con
```

### Start the container
```
docker start ol7_ords_con
```

### Remove the container
```
docker rm -vf ol7_ords_con
```

## Credits
Oracle-base docker files by [Tim Hall](https://github.com/oraclebase/dockerfiles)

## Changelog

#### 1.0.0 - Initial Release