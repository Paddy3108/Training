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