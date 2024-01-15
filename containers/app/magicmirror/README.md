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
