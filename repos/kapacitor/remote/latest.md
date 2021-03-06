## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:36fd87744439f3117dc9b324bb0312ea983b28149190babea5a3a2b226a295e1
```

-	Platforms:
	-	linux; amd64

### `kapacitor:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82011620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9d6890ddc7e327ab5085b7f79b5fcc83a85c5132d2acf36a4d019bb6de77cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 24 Apr 2017 19:20:41 GMT
ADD file:712c48086043553b85ffb031d8f6c5de857a2e53974df30cdfbc1e85c1b00a25 in / 
# Mon, 24 Apr 2017 19:20:42 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 19:54:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:25:06 GMT
RUN gpg     --keyserver hkp://ha.pool.sks-keyservers.net     --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5
# Tue, 25 Apr 2017 21:46:56 GMT
ENV KAPACITOR_VERSION=1.2.1
# Tue, 25 Apr 2017 21:47:04 GMT
RUN wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_amd64.deb.asc kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_amd64.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_amd64.deb*
# Tue, 25 Apr 2017 21:47:05 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 25 Apr 2017 21:47:06 GMT
EXPOSE 9092/tcp
# Tue, 25 Apr 2017 21:47:06 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 25 Apr 2017 21:47:07 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 25 Apr 2017 21:47:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Apr 2017 21:47:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cd0a524342efac6edff500c17e625735bbe479c926439b263bbe3c8518a0849c`  
		Last Modified: Mon, 24 Apr 2017 19:32:05 GMT  
		Size: 52.6 MB (52550276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39c3ffe41332a7a3c7f85f57e547361ec90b6e0091dd6058e06acccde2217d4`  
		Last Modified: Mon, 24 Apr 2017 22:19:28 GMT  
		Size: 19.3 MB (19266225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4715d1852381431f1f56c8cc181c1e32e13bfcf83cbee61bad195b55af9b5d`  
		Last Modified: Tue, 25 Apr 2017 16:56:35 GMT  
		Size: 6.8 KB (6787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db55e4ec391528835cfbbdf7127d9c0331c8c61f7897951f7ddefabab33f70e`  
		Last Modified: Tue, 25 Apr 2017 21:50:48 GMT  
		Size: 10.2 MB (10187876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a070a5530936fe9f558c1fbdc80c79aaeea13924c4c7b999131d19770e32f680`  
		Last Modified: Tue, 25 Apr 2017 21:50:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222df7757c7f15659900e7e68e58a4a24e238c9acb0330414f1b3d8a90712d92`  
		Last Modified: Tue, 25 Apr 2017 21:50:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
