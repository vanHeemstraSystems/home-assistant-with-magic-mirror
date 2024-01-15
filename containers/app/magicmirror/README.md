# MagicMirror 2

## 100 - Installation

### For server scenario

Open a shell and run:

```
$ cd run
$ cp serveronly.yml docker-compose.yml
```

## 200 - Starting Magic Mirror

### For server scenario

Navigate to ```~/magicmirror/run``` and execute:

```
$ docker compose up -d
```

The container will start. In server only mode opening a browser at http://localhost:8080 should show the MagicMirror (scenario server ☝️).

You can see the logs with

```
$ docker logs magicmirror
```

Executing

```
$ docker ps
```

will show all containers and

```
$ docker compose down
```

will stop and remove the MagicMirror container.

You can restart the container with one command ```docker compose up -d --force-recreate```. This is e.g. necessary if you change the configuration.

To get rid of all old images you can execute ```docker image prune -f```.

## Configuration

NOTE: To add a Open Weather API Key to the file ```/mounts/config/config.js`````` follow the instructions at https://openweathermap.org/api

After you have added **YOUR_OPENWEATHER_API_KEY**, do not forget to restart the Docker container with ```docker compose up -d --force-recreate``` for the new configuration to be picked up.

NOTE: You can find your location for the weather by looking into the file at http://bulk.openweathermap.org/sample/city.list.json.gz For example, Eindhoven (NL) has id: 2756252.
