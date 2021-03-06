## `rocket.chat:latest`

```console
$ docker pull rocket.chat@sha256:7dad79516253527935e023b1e2bdcd057c22e06b2fa791ad6431c78151f14952
```

-	Platforms:
	-	linux; amd64

### `rocket.chat:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199935253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a117a9069a51286144d2ec204910a31315b39ad0ed164f1bf47315cd164a4e`
-	Default Command: `["node","main.js"]`

```dockerfile
# Mon, 24 Apr 2017 19:20:41 GMT
ADD file:712c48086043553b85ffb031d8f6c5de857a2e53974df30cdfbc1e85c1b00a25 in / 
# Mon, 24 Apr 2017 19:20:42 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 19:54:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2017 02:33:32 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 25 Apr 2017 02:33:35 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     56730D5401028683275BD23C23EFEFE93C4CFFFE   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;   done
# Tue, 25 Apr 2017 02:33:50 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 03 May 2017 23:19:50 GMT
ENV NODE_VERSION=4.8.3
# Wed, 03 May 2017 23:20:03 GMT
RUN buildDeps='xz-utils'     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1     && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 03 May 2017 23:20:04 GMT
ENV YARN_VERSION=0.23.4
# Wed, 03 May 2017 23:20:09 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;   done   && curl -fSL -o yarn.js "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js"   && curl -fSL -o yarn.js.asc "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-legacy-$YARN_VERSION.js.asc"   && gpg --batch --verify yarn.js.asc yarn.js   && rm yarn.js.asc   && mv yarn.js /usr/local/bin/yarn   && chmod +x /usr/local/bin/yarn
# Wed, 03 May 2017 23:20:09 GMT
CMD ["node"]
# Thu, 04 May 2017 16:56:27 GMT
MAINTAINER buildmaster@rocket.chat
# Thu, 04 May 2017 16:56:29 GMT
RUN groupadd -r rocketchat &&  useradd -r -g rocketchat rocketchat &&  mkdir -p /app/uploads &&  chown rocketchat.rocketchat /app/uploads
# Thu, 04 May 2017 16:56:47 GMT
VOLUME [/app/uploads]
# Thu, 04 May 2017 16:56:49 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 0E163286C20D07B9787EBE9FD7F9D0414FD08104
# Thu, 04 May 2017 16:57:07 GMT
ENV RC_VERSION=0.55.1
# Thu, 04 May 2017 16:57:08 GMT
WORKDIR /app
# Thu, 04 May 2017 16:57:50 GMT
RUN curl -fSL "https://rocket.chat/releases/${RC_VERSION}/download" -o rocket.chat.tgz &&  curl -fSL "https://rocket.chat/releases/${RC_VERSION}/asc" -o rocket.chat.tgz.asc &&  gpg --batch --verify rocket.chat.tgz.asc rocket.chat.tgz &&  tar zxvf rocket.chat.tgz &&  rm rocket.chat.tgz rocket.chat.tgz.asc &&  cd bundle/programs/server &&  npm install
# Thu, 04 May 2017 16:58:16 GMT
USER [rocketchat]
# Thu, 04 May 2017 16:58:34 GMT
WORKDIR /app/bundle
# Thu, 04 May 2017 16:58:35 GMT
ENV MONGO_URL=mongodb://db:27017/meteor HOME=/tmp PORT=3000 ROOT_URL=http://localhost:3000 Accounts_AvatarStorePath=/app/uploads
# Thu, 04 May 2017 16:58:36 GMT
EXPOSE 3000/tcp
# Thu, 04 May 2017 16:58:37 GMT
CMD ["node" "main.js"]
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
	-	`sha256:f444da5fa2cdd81962d27a19802e984466379ab56d042c0040385274725cf4fe`  
		Last Modified: Tue, 25 Apr 2017 19:59:22 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ee8980874ac29ea494537573257a5dfc88599481c4996e4afab446a7945524`  
		Last Modified: Tue, 25 Apr 2017 19:59:23 GMT  
		Size: 119.2 KB (119152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0cb06f38d2454b74038083edf990b186d42815b64c42d18d3694aacd30773a`  
		Last Modified: Wed, 03 May 2017 23:39:37 GMT  
		Size: 12.6 MB (12578290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893ed87be4dbc5098553bb0584b308c35869f03590697dd37d2103248c305a46`  
		Last Modified: Wed, 03 May 2017 23:39:35 GMT  
		Size: 886.3 KB (886323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0ef95be6890e7c10069c67c8fdd2d03cad9d3c7847606edbf9205730a25ed9`  
		Last Modified: Thu, 04 May 2017 16:59:17 GMT  
		Size: 2.1 KB (2149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7588700fd0079d690a99917662d279c307ec70a02549bc331b2210ef204bde8`  
		Last Modified: Thu, 04 May 2017 16:59:16 GMT  
		Size: 127.2 KB (127204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4005989c63632fef804257b9671e3a0e79e4960ac86293ed5762e5c780692fe0`  
		Last Modified: Thu, 04 May 2017 16:59:45 GMT  
		Size: 114.4 MB (114401268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
