<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:14.04.5`](#ubuntu14045)
-	[`ubuntu:14.04`](#ubuntu1404)
-	[`ubuntu:trusty-20170330`](#ubuntutrusty-20170330)
-	[`ubuntu:trusty`](#ubuntutrusty)
-	[`ubuntu:16.04`](#ubuntu1604)
-	[`ubuntu:xenial-20170417.1`](#ubuntuxenial-201704171)
-	[`ubuntu:xenial`](#ubuntuxenial)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:16.10`](#ubuntu1610)
-	[`ubuntu:yakkety-20170327`](#ubuntuyakkety-20170327)
-	[`ubuntu:yakkety`](#ubuntuyakkety)
-	[`ubuntu:17.04`](#ubuntu1704)
-	[`ubuntu:zesty-20170411`](#ubuntuzesty-20170411)
-	[`ubuntu:zesty`](#ubuntuzesty)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:14.04.5`

```console
$ docker pull ubuntu@sha256:edf05697d8ea17028a69726b4b450ad48da8b29884cd640fec950c904bfb50ce
```

-	Platforms:
	-	linux; amd64

### `ubuntu:14.04.5` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65776178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302fa07d8117297adb599cc4ed7400348de5fe0f7950291e4bc32938324371b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Apr 2017 21:05:58 GMT
ADD file:cd830d3aacc66aa750a588e56d835663908f7fbb855cb96d00aa01feb9567948 in / 
# Wed, 12 Apr 2017 21:06:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 12 Apr 2017 21:06:02 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2017 21:06:03 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 12 Apr 2017 21:06:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 12 Apr 2017 21:06:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f229c550c2e1d5736aa23d1b3b5e10a70f9db72e4246867fd73271c11284b45`  
		Last Modified: Mon, 03 Apr 2017 14:21:42 GMT  
		Size: 65.7 MB (65703403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1fb71e8df6645b62584c22e511df7717c8fcc1c111b5dea1df60eda9b22c42`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 71.6 KB (71565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75a345868568d65d520f0ca596863dc6906460eb1ce68209fc9f85bb1ccf04d`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8744e322b832a60fc910434a6cb371a45e176fc08c93604878357302b709945c`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5165bfce78f4e197b6aedf3bcae095bd466ed7f7de688cd0710fa6875a699ab`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:14.04`

```console
$ docker pull ubuntu@sha256:edf05697d8ea17028a69726b4b450ad48da8b29884cd640fec950c904bfb50ce
```

-	Platforms:
	-	linux; amd64

### `ubuntu:14.04` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65776178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302fa07d8117297adb599cc4ed7400348de5fe0f7950291e4bc32938324371b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Apr 2017 21:05:58 GMT
ADD file:cd830d3aacc66aa750a588e56d835663908f7fbb855cb96d00aa01feb9567948 in / 
# Wed, 12 Apr 2017 21:06:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 12 Apr 2017 21:06:02 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2017 21:06:03 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 12 Apr 2017 21:06:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 12 Apr 2017 21:06:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f229c550c2e1d5736aa23d1b3b5e10a70f9db72e4246867fd73271c11284b45`  
		Last Modified: Mon, 03 Apr 2017 14:21:42 GMT  
		Size: 65.7 MB (65703403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1fb71e8df6645b62584c22e511df7717c8fcc1c111b5dea1df60eda9b22c42`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 71.6 KB (71565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75a345868568d65d520f0ca596863dc6906460eb1ce68209fc9f85bb1ccf04d`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8744e322b832a60fc910434a6cb371a45e176fc08c93604878357302b709945c`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5165bfce78f4e197b6aedf3bcae095bd466ed7f7de688cd0710fa6875a699ab`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty-20170330`

```console
$ docker pull ubuntu@sha256:edf05697d8ea17028a69726b4b450ad48da8b29884cd640fec950c904bfb50ce
```

-	Platforms:
	-	linux; amd64

### `ubuntu:trusty-20170330` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65776178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302fa07d8117297adb599cc4ed7400348de5fe0f7950291e4bc32938324371b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Apr 2017 21:05:58 GMT
ADD file:cd830d3aacc66aa750a588e56d835663908f7fbb855cb96d00aa01feb9567948 in / 
# Wed, 12 Apr 2017 21:06:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 12 Apr 2017 21:06:02 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2017 21:06:03 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 12 Apr 2017 21:06:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 12 Apr 2017 21:06:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f229c550c2e1d5736aa23d1b3b5e10a70f9db72e4246867fd73271c11284b45`  
		Last Modified: Mon, 03 Apr 2017 14:21:42 GMT  
		Size: 65.7 MB (65703403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1fb71e8df6645b62584c22e511df7717c8fcc1c111b5dea1df60eda9b22c42`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 71.6 KB (71565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75a345868568d65d520f0ca596863dc6906460eb1ce68209fc9f85bb1ccf04d`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8744e322b832a60fc910434a6cb371a45e176fc08c93604878357302b709945c`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5165bfce78f4e197b6aedf3bcae095bd466ed7f7de688cd0710fa6875a699ab`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:edf05697d8ea17028a69726b4b450ad48da8b29884cd640fec950c904bfb50ce
```

-	Platforms:
	-	linux; amd64

### `ubuntu:trusty` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65776178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302fa07d8117297adb599cc4ed7400348de5fe0f7950291e4bc32938324371b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Apr 2017 21:05:58 GMT
ADD file:cd830d3aacc66aa750a588e56d835663908f7fbb855cb96d00aa01feb9567948 in / 
# Wed, 12 Apr 2017 21:06:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 12 Apr 2017 21:06:02 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2017 21:06:03 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 12 Apr 2017 21:06:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 12 Apr 2017 21:06:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8f229c550c2e1d5736aa23d1b3b5e10a70f9db72e4246867fd73271c11284b45`  
		Last Modified: Mon, 03 Apr 2017 14:21:42 GMT  
		Size: 65.7 MB (65703403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1fb71e8df6645b62584c22e511df7717c8fcc1c111b5dea1df60eda9b22c42`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 71.6 KB (71565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75a345868568d65d520f0ca596863dc6906460eb1ce68209fc9f85bb1ccf04d`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8744e322b832a60fc910434a6cb371a45e176fc08c93604878357302b709945c`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5165bfce78f4e197b6aedf3bcae095bd466ed7f7de688cd0710fa6875a699ab`  
		Last Modified: Wed, 12 Apr 2017 21:09:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.04`

```console
$ docker pull ubuntu@sha256:f3a61450ae43896c4332bda5e78b453f4a93179045f20c8181043b26b5e79028
```

-	Platforms:
	-	linux; amd64

### `ubuntu:16.04` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b3f317ec734a73deca91b34c2b1e3dd7454650da9c8ef3047d29a873865178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:56:51 GMT
ADD file:141408db9037263a47322d1d78006be6a93927ac912bf14cd85100aa91da0421 in / 
# Mon, 24 Apr 2017 22:57:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:06 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:08 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aafe6b5e13de557451e1781fe7276620275625f970015cbd10036ab7d8ae27c0`  
		Last Modified: Thu, 20 Apr 2017 10:34:07 GMT  
		Size: 46.8 MB (46792902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b43a726608d3835aa027bbe181624789130c212eb191baa481f1d788a0676`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 815.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bdd1e546d21240bd4c3e4e29032a38f18102d780a78686508d40fe01c60158`  
		Last Modified: Mon, 24 Apr 2017 23:02:16 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8198342c3e05101bb56b0a585dc34e39346ece39ee5d39287cda24b1fb445fed`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56970a44fd409805e3872cac236d29f5eed1a45e189bb765bcd2163c915f384`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial-20170417.1`

```console
$ docker pull ubuntu@sha256:f3a61450ae43896c4332bda5e78b453f4a93179045f20c8181043b26b5e79028
```

-	Platforms:
	-	linux; amd64

### `ubuntu:xenial-20170417.1` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b3f317ec734a73deca91b34c2b1e3dd7454650da9c8ef3047d29a873865178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:56:51 GMT
ADD file:141408db9037263a47322d1d78006be6a93927ac912bf14cd85100aa91da0421 in / 
# Mon, 24 Apr 2017 22:57:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:06 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:08 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aafe6b5e13de557451e1781fe7276620275625f970015cbd10036ab7d8ae27c0`  
		Last Modified: Thu, 20 Apr 2017 10:34:07 GMT  
		Size: 46.8 MB (46792902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b43a726608d3835aa027bbe181624789130c212eb191baa481f1d788a0676`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 815.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bdd1e546d21240bd4c3e4e29032a38f18102d780a78686508d40fe01c60158`  
		Last Modified: Mon, 24 Apr 2017 23:02:16 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8198342c3e05101bb56b0a585dc34e39346ece39ee5d39287cda24b1fb445fed`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56970a44fd409805e3872cac236d29f5eed1a45e189bb765bcd2163c915f384`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial`

```console
$ docker pull ubuntu@sha256:f3a61450ae43896c4332bda5e78b453f4a93179045f20c8181043b26b5e79028
```

-	Platforms:
	-	linux; amd64

### `ubuntu:xenial` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b3f317ec734a73deca91b34c2b1e3dd7454650da9c8ef3047d29a873865178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:56:51 GMT
ADD file:141408db9037263a47322d1d78006be6a93927ac912bf14cd85100aa91da0421 in / 
# Mon, 24 Apr 2017 22:57:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:06 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:08 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aafe6b5e13de557451e1781fe7276620275625f970015cbd10036ab7d8ae27c0`  
		Last Modified: Thu, 20 Apr 2017 10:34:07 GMT  
		Size: 46.8 MB (46792902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b43a726608d3835aa027bbe181624789130c212eb191baa481f1d788a0676`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 815.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bdd1e546d21240bd4c3e4e29032a38f18102d780a78686508d40fe01c60158`  
		Last Modified: Mon, 24 Apr 2017 23:02:16 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8198342c3e05101bb56b0a585dc34e39346ece39ee5d39287cda24b1fb445fed`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56970a44fd409805e3872cac236d29f5eed1a45e189bb765bcd2163c915f384`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:f3a61450ae43896c4332bda5e78b453f4a93179045f20c8181043b26b5e79028
```

-	Platforms:
	-	linux; amd64

### `ubuntu:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46795242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b3f317ec734a73deca91b34c2b1e3dd7454650da9c8ef3047d29a873865178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:56:51 GMT
ADD file:141408db9037263a47322d1d78006be6a93927ac912bf14cd85100aa91da0421 in / 
# Mon, 24 Apr 2017 22:57:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:06 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:08 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aafe6b5e13de557451e1781fe7276620275625f970015cbd10036ab7d8ae27c0`  
		Last Modified: Thu, 20 Apr 2017 10:34:07 GMT  
		Size: 46.8 MB (46792902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b43a726608d3835aa027bbe181624789130c212eb191baa481f1d788a0676`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 815.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bdd1e546d21240bd4c3e4e29032a38f18102d780a78686508d40fe01c60158`  
		Last Modified: Mon, 24 Apr 2017 23:02:16 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8198342c3e05101bb56b0a585dc34e39346ece39ee5d39287cda24b1fb445fed`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56970a44fd409805e3872cac236d29f5eed1a45e189bb765bcd2163c915f384`  
		Last Modified: Mon, 24 Apr 2017 23:02:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.10`

```console
$ docker pull ubuntu@sha256:7fad1abb80626f62e3afb78faa79fb8bd0a2a5d10c4393b2087ba1189f001664
```

-	Platforms:
	-	linux; amd64

### `ubuntu:16.10` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42507226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1ddabad182e52730e29971284da6bd1b580415cdf343a535ee3879204128ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:57:48 GMT
ADD file:06609423c35881998d648352702e91a90aac71a764d875e8548774906d24447c in / 
# Mon, 24 Apr 2017 22:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:53 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c33899b2bc22cb5fa3fd6762134c9ae61a02d82c40e4e505b2217a7128fecf85`  
		Last Modified: Mon, 24 Apr 2017 23:03:52 GMT  
		Size: 42.5 MB (42504878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c357a45506793dea5b84d4ba9f5f2ae1702d8d8cc684189ab4983a338b5369`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ad21462d47b4dce2d58dfdcea2b0a91e07eed747909103a2880354f7dd882`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53272eb5cbaf78e89734e2b4467fea5d631b426042ca7349ecf22b5162d2880`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367354b20baabf1bd0e5336b500585eb5d53978297469bcd7c6a5854394a6de`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:yakkety-20170327`

```console
$ docker pull ubuntu@sha256:7fad1abb80626f62e3afb78faa79fb8bd0a2a5d10c4393b2087ba1189f001664
```

-	Platforms:
	-	linux; amd64

### `ubuntu:yakkety-20170327` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42507226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1ddabad182e52730e29971284da6bd1b580415cdf343a535ee3879204128ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:57:48 GMT
ADD file:06609423c35881998d648352702e91a90aac71a764d875e8548774906d24447c in / 
# Mon, 24 Apr 2017 22:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:53 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c33899b2bc22cb5fa3fd6762134c9ae61a02d82c40e4e505b2217a7128fecf85`  
		Last Modified: Mon, 24 Apr 2017 23:03:52 GMT  
		Size: 42.5 MB (42504878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c357a45506793dea5b84d4ba9f5f2ae1702d8d8cc684189ab4983a338b5369`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ad21462d47b4dce2d58dfdcea2b0a91e07eed747909103a2880354f7dd882`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53272eb5cbaf78e89734e2b4467fea5d631b426042ca7349ecf22b5162d2880`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367354b20baabf1bd0e5336b500585eb5d53978297469bcd7c6a5854394a6de`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:yakkety`

```console
$ docker pull ubuntu@sha256:7fad1abb80626f62e3afb78faa79fb8bd0a2a5d10c4393b2087ba1189f001664
```

-	Platforms:
	-	linux; amd64

### `ubuntu:yakkety` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42507226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1ddabad182e52730e29971284da6bd1b580415cdf343a535ee3879204128ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:57:48 GMT
ADD file:06609423c35881998d648352702e91a90aac71a764d875e8548774906d24447c in / 
# Mon, 24 Apr 2017 22:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:57:53 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:57:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:57:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:57:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c33899b2bc22cb5fa3fd6762134c9ae61a02d82c40e4e505b2217a7128fecf85`  
		Last Modified: Mon, 24 Apr 2017 23:03:52 GMT  
		Size: 42.5 MB (42504878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c357a45506793dea5b84d4ba9f5f2ae1702d8d8cc684189ab4983a338b5369`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9ad21462d47b4dce2d58dfdcea2b0a91e07eed747909103a2880354f7dd882`  
		Last Modified: Mon, 24 Apr 2017 23:03:45 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53272eb5cbaf78e89734e2b4467fea5d631b426042ca7349ecf22b5162d2880`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367354b20baabf1bd0e5336b500585eb5d53978297469bcd7c6a5854394a6de`  
		Last Modified: Mon, 24 Apr 2017 23:03:46 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:17.04`

```console
$ docker pull ubuntu@sha256:a5a0e5c797e831f448307fecacbed7d0b66bf127e8e83a037381fb00a6dff858
```

-	Platforms:
	-	linux; amd64

### `ubuntu:17.04` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37471677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31f19d079cc41116bd96fa9d093bd25bb7c680caef3a3d07d5f96f20a9565bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:58:36 GMT
ADD file:0580427668b7fda8b57b8191d117f8bbda00acd9e921beef670800838c9e57c1 in / 
# Mon, 24 Apr 2017 22:58:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:58:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:58:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:58:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:58:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a5614abc69121e3be2e6f070ee104cf18e716d860d5ac8dc7f5d4b0b45d4eeb`  
		Last Modified: Mon, 24 Apr 2017 23:04:56 GMT  
		Size: 37.5 MB (37469402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d067130d8e89de718726a2c26184b3906f191139887e034bc53fa2b2a0323`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831c7598833c1494ca1cf9f342daefdfd37f1dabff9518ef579b09fa643c3aa2`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a410fc1d3bfe19c7c29a947bcdcd46a44bc2e2756d977ae7a6f154bc22fa92a`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3271f041ee12253944506a40ac433c9642778b8f13d54fa782f19dc1f5ee160c`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:zesty-20170411`

```console
$ docker pull ubuntu@sha256:a5a0e5c797e831f448307fecacbed7d0b66bf127e8e83a037381fb00a6dff858
```

-	Platforms:
	-	linux; amd64

### `ubuntu:zesty-20170411` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37471677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31f19d079cc41116bd96fa9d093bd25bb7c680caef3a3d07d5f96f20a9565bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:58:36 GMT
ADD file:0580427668b7fda8b57b8191d117f8bbda00acd9e921beef670800838c9e57c1 in / 
# Mon, 24 Apr 2017 22:58:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:58:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:58:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:58:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:58:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a5614abc69121e3be2e6f070ee104cf18e716d860d5ac8dc7f5d4b0b45d4eeb`  
		Last Modified: Mon, 24 Apr 2017 23:04:56 GMT  
		Size: 37.5 MB (37469402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d067130d8e89de718726a2c26184b3906f191139887e034bc53fa2b2a0323`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831c7598833c1494ca1cf9f342daefdfd37f1dabff9518ef579b09fa643c3aa2`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a410fc1d3bfe19c7c29a947bcdcd46a44bc2e2756d977ae7a6f154bc22fa92a`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3271f041ee12253944506a40ac433c9642778b8f13d54fa782f19dc1f5ee160c`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:zesty`

```console
$ docker pull ubuntu@sha256:a5a0e5c797e831f448307fecacbed7d0b66bf127e8e83a037381fb00a6dff858
```

-	Platforms:
	-	linux; amd64

### `ubuntu:zesty` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37471677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31f19d079cc41116bd96fa9d093bd25bb7c680caef3a3d07d5f96f20a9565bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:58:36 GMT
ADD file:0580427668b7fda8b57b8191d117f8bbda00acd9e921beef670800838c9e57c1 in / 
# Mon, 24 Apr 2017 22:58:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:58:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:58:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:58:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:58:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a5614abc69121e3be2e6f070ee104cf18e716d860d5ac8dc7f5d4b0b45d4eeb`  
		Last Modified: Mon, 24 Apr 2017 23:04:56 GMT  
		Size: 37.5 MB (37469402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d067130d8e89de718726a2c26184b3906f191139887e034bc53fa2b2a0323`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831c7598833c1494ca1cf9f342daefdfd37f1dabff9518ef579b09fa643c3aa2`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a410fc1d3bfe19c7c29a947bcdcd46a44bc2e2756d977ae7a6f154bc22fa92a`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3271f041ee12253944506a40ac433c9642778b8f13d54fa782f19dc1f5ee160c`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:a5a0e5c797e831f448307fecacbed7d0b66bf127e8e83a037381fb00a6dff858
```

-	Platforms:
	-	linux; amd64

### `ubuntu:rolling` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37471677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31f19d079cc41116bd96fa9d093bd25bb7c680caef3a3d07d5f96f20a9565bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 24 Apr 2017 22:58:36 GMT
ADD file:0580427668b7fda8b57b8191d117f8bbda00acd9e921beef670800838c9e57c1 in / 
# Mon, 24 Apr 2017 22:58:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 24 Apr 2017 22:58:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 24 Apr 2017 22:58:56 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 24 Apr 2017 22:58:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 24 Apr 2017 22:58:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a5614abc69121e3be2e6f070ee104cf18e716d860d5ac8dc7f5d4b0b45d4eeb`  
		Last Modified: Mon, 24 Apr 2017 23:04:56 GMT  
		Size: 37.5 MB (37469402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d067130d8e89de718726a2c26184b3906f191139887e034bc53fa2b2a0323`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831c7598833c1494ca1cf9f342daefdfd37f1dabff9518ef579b09fa643c3aa2`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a410fc1d3bfe19c7c29a947bcdcd46a44bc2e2756d977ae7a6f154bc22fa92a`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3271f041ee12253944506a40ac433c9642778b8f13d54fa782f19dc1f5ee160c`  
		Last Modified: Mon, 24 Apr 2017 23:04:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
