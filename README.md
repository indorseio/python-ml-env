# Project Python Machine Learning Environment

[Docker Compose](https://docs.docker.com/compose/install/) is needed to set up this project on
dev machine.

----
## Commands

To start the docker container
```sh
$ docker-compose up
```

To build/rebuild the docker container
```sh
$ docker-compose build
```

To login into python container
```sh
docker exec -it $(docker ps | grep "python-ml-env_api" | awk '{print $1}') bash
```

#### Steps to run machine learning claims ####

1. Clone the specific claim in the claims directory.
2. Add the requirements in the requirements.txt directory.
3. Build/rebuild the docker container
4. Login to the python shell.
    ```sh
    docker exec -it $(docker ps | grep "python-ml-env_api" | awk '{print $1}') bash
    ```
5. From this shell, run the commands as specified in the claimant's repo readme file.

6. To change the Python version, modify the line number 1 of Dockerfile.


### Good Ideas ###
1. Search for the library in the website https://pypi.org.
2. Then match the specified version as per the claimant's repo readme file.
3. It should be available.
4. If it is available, then add the same requirement in requirements.txt.
 

