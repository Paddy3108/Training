# Part 1
## 1.1

```
C:\>docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS                          PORTS               NAMES
d64b363f518a        java                "/bin/bash"              18 seconds ago       Exited (0) 17 seconds ago                           festive_noether
e8dfb68eb667        node                "docker-entrypoint.s…"   About a minute ago   Exited (0) About a minute ago                       ecstatic_lamport
1d04e56fffb6        nginx               "/docker-entrypoint.…"   6 minutes ago        Exited (0) 5 minutes ago                            crazy_sutherland
```

## 1.2
```
C:\>docker ps -as
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES               SIZE

C:\>docker images
REPOSITORY                    TAG                 IMAGE ID            CREATED             SIZE
```

## 1.3
```
C:\>docker run -it devopsdockeruh/pull_exercise
Unable to find image 'devopsdockeruh/pull_exercise:latest' locally
latest: Pulling from devopsdockeruh/pull_exercise
8e402f1a9c57: Pull complete                                                                                                                                                                                                      5e2195587d10: Pull complete                                                                                                                                                                                                      6f595b2fc66d: Pull complete                                                                                                                                                                                                      165f32bf4e94: Pull complete                                                                                                                                                                                                      67c4f504c224: Pull complete                                                                                                                                                                                                      Digest: sha256:7c0635934049afb9ca0481fb6a58b16100f990a0d62c8665b9cfb5c9ada8a99f
Status: Downloaded newer image for devopsdockeruh/pull_exercise:latest
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
```

## 1.4
```
C:\>docker run -d --name ex14 devopsdockeruh/exec_bash_exercise
e5f8941499ef600c9726c5181604e0425087ce2a2ea485f44cc25c04a3aa3590

C:\>docker exec -it ex14 bash
root@e5f8941499ef:/usr/app# tail -f logs.txt
"Docker is easy"
Tue, 14 Jul 2020 12:00:31 GMT
Tue, 14 Jul 2020 12:00:34 GMT
Tue, 14 Jul 2020 12:00:37 GMT
Tue, 14 Jul 2020 12:00:40 GMT
Secret message is:
"Docker is easy"
```

## 1.5
Assuming included file `Dockerfile5`.

```
path:\> docker build -f Dockerfile5 -t ex5 .
path:\>docker run -it --rm ex5
root@da2da7f65415:/# sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```

## 1.6
Assuming included file `Dockerfile6`.

```
path:\> docker build -f Dockerfile6 -t  docker-clock .
[...]
Successfully tagged docker-clock:latest
path:\>docker run docker-clock
1
2
3
4
5
6
[..]
```

## 1.7
Assuming included file `Dockerfile7`.

```
path:\> docker build -f Dockerfile7 -t  curler .
Input website:
helsinki.fi
: bad variable name
Searching..
sleep: invalid time interval '1\r'
Try 'sleep --help' for more information.
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```

## 1.8
```
path:\>docker run -it --rm -v "%cd%"/log.txt:/usr/app/logs.txt devopsdockeruh/first_volume_exercise
Wrote to file /usr/app/logs.txt
^CClosing file
```

## 1.9
```
path:\>docker run -d --rm -p 8080:80 devopsdockeruh/ports_exercise
Unable to find image 'devopsdockeruh/ports_exercise:latest' locally
latest: Pulling from devopsdockeruh/ports_exercise
cbdbe7a5bc2a: Pull complete                                                                                             fb0e3739aee1: Pull complete                                                                                             738de7869598: Pull complete                                                                                             ffd68be3d86c: Pull complete                                                                                             d6a92ac5065d: Pull complete                                                                                             8deb0960be38: Pull complete                                                                                             aec7a3bd83e0: Pull complete                                                                                             8f73392c117e: Pull complete                                                                                             Digest: sha256:9779e303353ef47da9ea0223bfbb9fbdb8f8fe39178e2e06153027e28e9e5400
Status: Downloaded newer image for devopsdockeruh/ports_exercise:latest
893439b3fe64c44107b34c9ff1d78e5729d26978769ac52caa2cf7d15086451c

path:\>curl http://localhost:8080
Ports configured correctly!!
```

## 1.10
Assuming included file `Dockerfile10`.

```
path\frontend-example-docker-master>docker build -f "path\Dockerfile10" -t ex10 .
path:\>docker run --rm -p 5000:5000 ex10:latest
```

## 1.11
Code wasn't startable. I moved `cross-env` from `devDependencies` to `dependencies` in `package.json`. After that the application was valid. 

See included `Dockerfile11`.

```
path\backend-example-docker-master>docker build -f "path\Dockerfile11" -t ex11 .
path:\>docker run --rm -p 8000:8000 -v "%cd%"/tmp/log.txt:/home/node/logs.txt ex11
```

## 1.12
Assuming included files `Dockerfile10` and `Dockerfile11`.

```
path:\>docker run -d --rm --name front -p 5000:5000 -e API_URL=http://localhost:8000/ ex10:latest

path:\>docker run -d --rm --name back -p 8000:8000 -e FRONT_URL=http://localhost:5000 -v "%cd%"/tmp/log.txt:/home/node/logs.txt ex11:latest

```

## 1.13
Assuming included file `Dockerfile13`.

```
path\spring-example-project-master>docker build -f "path\Dockerfile13" -t ex13 .
path:\>docker run -d --rm -p 8080:8080 ex13:latest
```

## 1.14 
Assuming included file `Dockerfile14`

```
path\rails-example-project-master>docker build -f "path\Dockerfile14" -t ex14 .
path:\>docker run -d --rm -p 3000:3000 ex14:latest
```

## 1.15
[Docker Hub](https://hub.docker.com/r/paddy310896/hello-world)

## 1.16
[Heroku](https://paddy3108-heroku-example.herokuapp.com/)

## 1.7
Skipped