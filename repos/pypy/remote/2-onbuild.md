## `pypy:2-onbuild`

```console
$ docker pull pypy@sha256:fed41830c7e259a3145e34b078ffacbade63232fe83707314ae7fe2d99300134
```

-	Platforms:
	-	linux; amd64

### `pypy:2-onbuild` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278244992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ab6d3b0423b22b665df03ef68db2eb5dd866e9bdb71eaaa0c5aa2ce86c25a6`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 24 Apr 2017 19:20:41 GMT
ADD file:712c48086043553b85ffb031d8f6c5de857a2e53974df30cdfbc1e85c1b00a25 in / 
# Mon, 24 Apr 2017 19:20:42 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 19:54:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 19:55:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2017 04:45:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Apr 2017 04:45:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Apr 2017 04:45:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tcl 		tk 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2017 14:03:03 GMT
ENV PYPY_VERSION=5.7.1
# Tue, 25 Apr 2017 14:03:04 GMT
ENV PYPY_SHA256SUM=c4fa3da42156bed4a9d912433b618a141e0c5161d7cc8c328786736ea5d1c2da
# Tue, 25 Apr 2017 14:03:05 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 25 Apr 2017 14:03:25 GMT
RUN set -ex 	&& wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2-v${PYPY_VERSION}-linux64.tar.bz2" 	&& echo "$PYPY_SHA256SUM  pypy.tar.bz2" | sha256sum -c 	&& tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2 	&& rm pypy.tar.bz2 			&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& pypy /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	&& pip install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& rm -rf ~/.cache
# Tue, 25 Apr 2017 14:03:26 GMT
CMD ["pypy"]
# Tue, 25 Apr 2017 14:04:17 GMT
RUN mkdir -p /usr/src/app
# Tue, 25 Apr 2017 14:04:17 GMT
WORKDIR /usr/src/app
# Tue, 25 Apr 2017 14:04:18 GMT
ONBUILD COPY requirements.txt /usr/src/app/
# Tue, 25 Apr 2017 14:04:35 GMT
ONBUILD RUN pip install -r requirements.txt
# Tue, 25 Apr 2017 14:04:36 GMT
ONBUILD COPY . /usr/src/app
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
	-	`sha256:85334a7c200103c122f3cbf56460f28fe688abc52655dc714afa939e49848ba8`  
		Last Modified: Mon, 24 Apr 2017 22:20:21 GMT  
		Size: 43.2 MB (43231315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c546d9d6a84ca2a1b7459a47978abe757bf67096d9dd704a9a5a0a786d2d325`  
		Last Modified: Mon, 24 Apr 2017 22:21:26 GMT  
		Size: 131.8 MB (131793725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb12d55dae45affbf26acf2312ce43b372d901adbe39df0a0d565a4ded93be`  
		Last Modified: Tue, 25 Apr 2017 05:07:40 GMT  
		Size: 2.9 MB (2902257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77750db93368aaedb79b61d47ab88f161b2ac09d5890ec56956938acf4df316`  
		Last Modified: Tue, 25 Apr 2017 21:03:08 GMT  
		Size: 28.5 MB (28501068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c06d65ceb90b19d54f099f2b9fca58ae15b9532382c093a44dd0ddcbb94ea55`  
		Last Modified: Tue, 25 Apr 2017 21:04:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
