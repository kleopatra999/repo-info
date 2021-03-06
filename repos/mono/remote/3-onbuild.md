## `mono:3-onbuild`

```console
$ docker pull mono@sha256:98f8fe6573567f82da744ffb2cef170a3aa7657c9ac104d18240aacd1bc8e435
```

-	Platforms:
	-	linux; amd64

### `mono:3-onbuild` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128149320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf2c111fbe824119d2f130a40bbaaca881df8171a1eef8ffb36179790de507`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 19:30:04 GMT
ADD file:cda477892272e4acea1f147bb76a3de26ec0d0abfd0c8c4171bfb10053c98985 in / 
# Mon, 24 Apr 2017 19:30:04 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 23:53:50 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 24 Apr 2017 23:54:04 GMT
RUN apt-get update 	&& apt-get install -y curl 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 23:54:06 GMT
RUN apt-key adv --keyserver pgp.mit.edu --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 24 Apr 2017 23:55:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/3.12.0 main" > /etc/apt/sources.list.d/mono-xamarin.list         && echo "deb http://download.mono-project.com/repo/debian 312-security main" >> /etc/apt/sources.list.d/mono-xamarin.list 	&& apt-get update 	&& apt-get install -y mono-devel ca-certificates-mono fsharp mono-vbnc nuget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 23:55:24 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 24 Apr 2017 23:55:25 GMT
RUN mkdir -p /usr/src/app/source /usr/src/app/build
# Mon, 24 Apr 2017 23:55:26 GMT
WORKDIR /usr/src/app/source
# Mon, 24 Apr 2017 23:55:26 GMT
ONBUILD COPY . /usr/src/app/source
# Mon, 24 Apr 2017 23:55:27 GMT
ONBUILD RUN nuget restore -NonInteractive
# Mon, 24 Apr 2017 23:55:28 GMT
ONBUILD RUN xbuild /property:Configuration=Release /property:OutDir=/usr/src/app/build/
# Mon, 24 Apr 2017 23:55:28 GMT
ONBUILD WORKDIR /usr/src/app/build
```

-	Layers:
	-	`sha256:1d46ed2a74b7da1620376a8b57cf77856ed64160d01186fc015979796e664085`  
		Last Modified: Mon, 24 Apr 2017 19:41:46 GMT  
		Size: 38.1 MB (38117052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9937cb766189b1a7f9c45b1476a641da575179a4f9cc36a85d132083c8d13315`  
		Last Modified: Tue, 25 Apr 2017 18:47:38 GMT  
		Size: 7.8 MB (7759592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ec8f286db72b737ed4f90d93c5b3851245d2db8dff8be62f74e4976f3d8afb`  
		Last Modified: Tue, 25 Apr 2017 18:47:35 GMT  
		Size: 29.9 KB (29903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f82dd9682b4de1d0b8f1b1dd0135a53edb65539183c50e415eae07fae63e6`  
		Last Modified: Tue, 25 Apr 2017 18:49:41 GMT  
		Size: 82.2 MB (82242611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9642649777350c52261de543be54e77d2ce642711055cecff72e79b2cd2e3b52`  
		Last Modified: Tue, 25 Apr 2017 18:51:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
