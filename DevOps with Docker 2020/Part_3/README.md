# Part 3
## 3.1

Frontend
```
H:\>docker history ex10
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
2f422c7c87f7        5 days ago          /bin/sh -c #(nop)  ENTRYPOINT ["npm" "start"]   0B
0a82531421eb        5 days ago          /bin/sh -c set -x   && npm install   && npm …   247MB
a7512cda4d90        5 days ago          /bin/sh -c #(nop) ADD dir:1fb79da7abb78390dd…   557kB
156f9bc89aed        8 days ago          /bin/sh -c #(nop)  ENV NODE_ENV=production      0B
bba05d82d993        8 days ago          /bin/sh -c #(nop) WORKDIR /home/node            0B
eb93aaaee71f        8 days ago          /bin/sh -c #(nop)  EXPOSE 5000                  0B
28367a45b626        8 days ago          /bin/sh -c #(nop)  USER node                    0B
6bf4087f2679        7 weeks ago         /bin/sh -c #(nop)  CMD ["node"]                 0B
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENTRYPOINT ["docker-entry…   0B
<missing>           7 weeks ago         /bin/sh -c #(nop) COPY file:238737301d473041…   116B
<missing>           7 weeks ago         /bin/sh -c apk add --no-cache --virtual .bui…   8.34MB
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENV YARN_VERSION=1.22.4      0B
<missing>           7 weeks ago         /bin/sh -c addgroup -g 1000 node     && addu…   69.9MB
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENV NODE_VERSION=10.21.0     0B
<missing>           3 months ago        /bin/sh -c #(nop)  CMD ["/bin/sh"]              0B
<missing>           3 months ago        /bin/sh -c #(nop) ADD file:b91adb67b670d3a6f…   5.61MB
```
Backend

```
H:\>docker history ex11
IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
70e44137f478        8 days ago          /bin/sh -c #(nop)  ENTRYPOINT ["npm" "start"]   0B
999d4822cad7        8 days ago          /bin/sh -c set -x   && npm install              30.1MB
8de009a57f6e        8 days ago          /bin/sh -c #(nop) ADD dir:df74a88dc7476cd8e3…   220kB
90a2091cbaf7        8 days ago          /bin/sh -c #(nop)  ENV NODE_ENV=production      0B
452c74a6505a        8 days ago          /bin/sh -c #(nop) WORKDIR /home/node            0B
ef4295e063c7        8 days ago          /bin/sh -c #(nop)  EXPOSE 8000                  0B
28367a45b626        8 days ago          /bin/sh -c #(nop)  USER node                    0B
6bf4087f2679        7 weeks ago         /bin/sh -c #(nop)  CMD ["node"]                 0B
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENTRYPOINT ["docker-entry…   0B
<missing>           7 weeks ago         /bin/sh -c #(nop) COPY file:238737301d473041…   116B
<missing>           7 weeks ago         /bin/sh -c apk add --no-cache --virtual .bui…   8.34MB
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENV YARN_VERSION=1.22.4      0B
<missing>           7 weeks ago         /bin/sh -c addgroup -g 1000 node     && addu…   69.9MB
<missing>           7 weeks ago         /bin/sh -c #(nop)  ENV NODE_VERSION=10.21.0     0B
<missing>           3 months ago        /bin/sh -c #(nop)  CMD ["/bin/sh"]              0B
<missing>           3 months ago        /bin/sh -c #(nop) ADD file:b91adb67b670d3a6f…   5.61MB
```
## 3.2

## 3.3

## 3.4
[Dockerfile Backend](https://github.com/Paddy3108/Training/blob/training/docker/DevOps%20with%20Docker%202020/Part_3/4/Dockerfile_backend)[Dockerfile Frontend](https://github.com/Paddy3108/Training/blob/training/docker/DevOps%20with%20Docker%202020/Part_3/4/Dockerfile_frontend)

## 3.5

### Image sizes
| Image | Size (alpine) | Size (node) | 
| ------| :--------------:| :-----------:|
| Frontend | 308mb | 247mb|
| Backend | 95mb | 30mb|

