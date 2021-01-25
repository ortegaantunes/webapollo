# APOLLO

Apollo - A collaborative, real-time, genome annotation web-based editor.

The application’s technology stack includes a Grails-based Java web application with flexible database backends and a Javascript client that runs in a web browser as a JBrowse plugin.

You can find the latest release here: https://github.com/GMOD/Apollo/releases/latest and our setup guide: http://genomearchitect.readthedocs.io/en/latest/Setup.html

## Installation

This code has been using docker environment based in a image from Project owner. The project has some customizations to share directorys between host and container. The share was made to facilitate the add of news Organism and make backup actions easier.


```bash
Open the Terminal on your Operating System and execute the below command:

Ps: You need be on directory where the project was downloaded. Eg: /Users/Desktop/apollo

docker-compose -f docker-compose.yml -p apollo up -d --build
```

## Directory

The docker create a some directory in root directory. Is important remeber that this code is preparate to running in MacOS environment and this root directory is located on "C:". To customize to Unix system please replace the source directory in docker-compose.yml

## Docker for MacOS 

To do the docker installation on Windows please do the windows update to latest version and after that do the download and installation of Docker from the below link.

```python
# Please do the download and do the installation
Docker: https://hub.docker.com/editions/community/docker-ce-desktop-mac/
```

## Database

The default database is Postgresql and in the future we will create a script to do a dump from database.

## Access

The URL access is based on 8080 port and is based in Tomcat Webserver. Is possible do a reverse proxy with NGINX or Apache.

```bash
Link: http://localhost:8080
```

## Docker Command

To the first time is need to execute manual commands to build the infrastructure. Remember, this step is only on the first time.

Go to the directory where you saved the clone of the repository, like /Users/Documents/webapollo

After that run the command "ls" and make sure that in the repository has files with name: docker-compose.yml

Now you need execute the command: 

```bash
docker-compose up --build -d
```

The command will do the download of the original images from project source. It will take a while.


## Password

The default user is admin@local.host and password is password. It should be replace in the first login.

## Organism

To create a new organism you should copy the original files to root directory and sub-folder organism like: "/Users/apollo/organism/yeast", is important remember that the files should be extracted and must contain the trackList.json file.

In the Apollo sytem in Organism tab to create a new organism the section directory must be /opt/organism/organism_name, i.e: /opt/organism/yeast

## Users

To create a new users, you should have a Organism created. The users are authorization options to ensure the correct permissions.

