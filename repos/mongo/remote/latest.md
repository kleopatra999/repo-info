## `mongo:latest`

```console
$ docker pull mongo@sha256:04ff09008c6bf8f5e72600485a5d1b35ab0a1f9b28c53c8a6c7b1bc6a4189250
```

-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131909632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f03b16565e14412f4de1f9a5898a097bd906caaa5f31db846da4105325df03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 24 Apr 2017 19:21:19 GMT
ADD file:a13c726be90f637e04ad902f42b3a6d973309bf0c098eb82dda7e518adbd8833 in / 
# Mon, 24 Apr 2017 19:21:20 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 23:49:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Mon, 01 May 2017 18:37:35 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 May 2017 18:37:36 GMT
ENV GOSU_VERSION=1.7
# Mon, 01 May 2017 18:37:51 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Mon, 01 May 2017 18:37:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 01 May 2017 18:37:53 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Mon, 01 May 2017 18:37:56 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 01 May 2017 18:37:57 GMT
ENV MONGO_MAJOR=3.4
# Mon, 01 May 2017 18:37:57 GMT
ENV MONGO_VERSION=3.4.4
# Mon, 01 May 2017 18:37:58 GMT
ENV MONGO_PACKAGE=mongodb-org
# Mon, 01 May 2017 18:38:00 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Mon, 01 May 2017 18:38:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 01 May 2017 18:38:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 01 May 2017 18:38:19 GMT
VOLUME [/data/db /data/configdb]
# Mon, 01 May 2017 18:38:20 GMT
COPY file:7c445c3da5fdc0495368be2c40f1d2a4cd7590cf458336174c54b078324bb71f in /usr/local/bin/ 
# Mon, 01 May 2017 18:38:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 01 May 2017 18:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 May 2017 18:38:23 GMT
EXPOSE 27017/tcp
# Mon, 01 May 2017 18:38:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:47e616392c23265a5e531497d94557c2e269cf3ae5616c37fbe1a75bb02b40f4`  
		Last Modified: Mon, 24 Apr 2017 19:33:31 GMT  
		Size: 30.6 MB (30605723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dc044ce904d18c6e4abaee657e7ed9f9d400c6f85700b65929bbe1ef9526db`  
		Last Modified: Tue, 25 Apr 2017 00:16:13 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8484c3282b46d5ab254b86a9280cef3b14452d4c3c1d3647c8522ceb2181e1`  
		Last Modified: Mon, 01 May 2017 18:41:32 GMT  
		Size: 2.4 MB (2404770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95d3755f06a0214f73154fea5d2c4eb5fbe5d5177644408fd73c05cf2fe19c6`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 889.1 KB (889059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a477845b3b4c225b129eba586b2b7d675836f49d26e254f7485a91f6ac3966fb`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14c2ad4739341547c2f27054921c9aa5cfc7fed24e99e69df2e8b3711690b5c`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9a2d6977fa6a92bc0ba38e907268b9ba964358e14df7b96c7edee0fa4ec28a`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7df3703a745e3250d2460f247c811b451fedbe3cc50ac712cb701300acacdc`  
		Last Modified: Mon, 01 May 2017 18:41:47 GMT  
		Size: 98.0 MB (98003086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2fdfb53f629fd2781979bfb98de5650152f003775f93cff07369b3c243c165`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27b754732112bdb403f5f8e4077567607963ebfd3addbdfef33650327bc0520`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 2.9 KB (2909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef5fbd2b07516c0bd1f991f2639ac8a75e861d45132660799acdad8bb99a64e`  
		Last Modified: Mon, 01 May 2017 18:41:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
