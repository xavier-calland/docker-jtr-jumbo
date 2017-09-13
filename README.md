# docker-jtr-jumbo
Docker image with JohnTheRipper Jumbo with rockyou wordlist

## Supported tags and respective Dockerfile links

* [jtr-1.8.0](https://github.com/xavier-calland/docker-jtr-jumbo/blob/master/jtr-1.8.0/Dockerfile)


## Info

* Working directory is `/etc/jtr`
  * Relative paths are in this directory (pot, session, hash, …)
  * Mount a volume in `/etc/jtr` to share these files
* Rockyou file is in `/opt/jtr/dic/`


## Exemple

```
docker run  -u 1000:1000 -it -v `pwd`:/etc/jtr/ xaviercalland/docker-jtr-jumbo:jtr-1.8.0 hashes.txt --pot=crack.pot --fork=2 --rules --wordlist=/opt/jtr/dic/rockyou.dic
docker run  -u 1000:1000 -it -v `pwd`:/etc/jtr/ xaviercalland/docker-jtr-jumbo:jtr-1.8.0 hashes.txt --pot=crack.pot --fork=2 --markov=250:0:0:8
docker run  -u 1000:1000 -it -v `pwd`:/etc/jtr/ xaviercalland/docker-jtr-jumbo:jtr-1.8.0 --pot=crack.pot --show
```
