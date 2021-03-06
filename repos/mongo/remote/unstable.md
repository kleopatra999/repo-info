## `mongo:unstable`

```console
$ docker pull mongo@sha256:1bb1e8d131864151880356fe394db5c47c4ad1e5f57727d38f265b005ae1ee21
```

-	Platforms:
	-	linux; amd64

### `mongo:unstable` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133193680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7996f59f72706dea1dcfc0adf28991ef9390cfc42e9cf28004649a018ee019`
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
# Mon, 01 May 2017 18:38:42 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Mon, 01 May 2017 18:38:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Mon, 01 May 2017 18:38:46 GMT
ENV MONGO_MAJOR=3.5
# Mon, 01 May 2017 18:38:47 GMT
ENV MONGO_VERSION=3.5.6
# Mon, 01 May 2017 18:38:47 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable
# Mon, 01 May 2017 18:38:49 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Mon, 01 May 2017 18:39:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 01 May 2017 18:39:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 01 May 2017 18:39:09 GMT
VOLUME [/data/db /data/configdb]
# Mon, 01 May 2017 18:39:10 GMT
COPY file:7c445c3da5fdc0495368be2c40f1d2a4cd7590cf458336174c54b078324bb71f in /usr/local/bin/ 
# Mon, 01 May 2017 18:39:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 01 May 2017 18:39:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 May 2017 18:39:14 GMT
EXPOSE 27017/tcp
# Mon, 01 May 2017 18:39:14 GMT
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
	-	`sha256:d1db636d00e7e5a22f8ac6688a735c6e50fda8a1063fe2a99c28021be7786cf1`  
		Last Modified: Mon, 01 May 2017 18:43:11 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf5e4d2143644cdfd8e2f8a8877f594e1175c88fef026b1e3a4764a0eb8ab66`  
		Last Modified: Mon, 01 May 2017 18:43:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b0e5fe26ca16c2824d0eff2041510d59a12c8baf2ab724b95603eefcba0277`  
		Last Modified: Mon, 01 May 2017 18:43:26 GMT  
		Size: 99.3 MB (99287135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25029c729cd2212ee14af83c5f9032cb793c9ffe5a96f45aa37e472974b7b98`  
		Last Modified: Mon, 01 May 2017 18:43:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3516a30b2e209e7a91d1a07c86fe24ce895be2007b9ba9cfeef0dbd468901e6e`  
		Last Modified: Mon, 01 May 2017 18:43:10 GMT  
		Size: 2.9 KB (2908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26450f445075a32fe0cf2e0f3bb2d02b1d7ca5fe7a7b7e43efb5be0989fc1dd0`  
		Last Modified: Mon, 01 May 2017 18:43:10 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
