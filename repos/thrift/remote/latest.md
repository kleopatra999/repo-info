## `thrift:latest`

```console
$ docker pull thrift@sha256:4023120190ebfe123e392fd20e870864e02247942745001fa5f1fbf1c041c84a
```

-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51276202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566c673c4978cd6ed9d29c0496c4006de2bec41d23f9d971edaa06226c840626`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 24 Apr 2017 19:30:04 GMT
ADD file:cda477892272e4acea1f147bb76a3de26ec0d0abfd0c8c4171bfb10053c98985 in / 
# Mon, 24 Apr 2017 19:30:04 GMT
CMD ["/bin/bash"]
# Tue, 25 Apr 2017 05:50:19 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 25 Apr 2017 05:50:19 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 25 Apr 2017 05:53:21 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Apr 2017 05:53:22 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:1d46ed2a74b7da1620376a8b57cf77856ed64160d01186fc015979796e664085`  
		Last Modified: Mon, 24 Apr 2017 19:41:46 GMT  
		Size: 38.1 MB (38117052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcea7e415a8803d5d9bb578d7d3aceb158c19e920368b527241c6bb5a395f22b`  
		Last Modified: Tue, 25 Apr 2017 22:08:18 GMT  
		Size: 13.2 MB (13159150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
