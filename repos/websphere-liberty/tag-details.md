<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:microProfile`](#websphere-libertymicroprofile)
-	[`websphere-liberty:webProfile6`](#websphere-libertywebprofile6)
-	[`websphere-liberty:webProfile7`](#websphere-libertywebprofile7)
-	[`websphere-liberty:javaee7`](#websphere-libertyjavaee7)
-	[`websphere-liberty:latest`](#websphere-libertylatest)
-	[`websphere-liberty:beta`](#websphere-libertybeta)

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:d0faf400d493245f2f217a3216ee61abd8df73a6ba4e7db402801c186ce7643d
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:kernel` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172773337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9b1014b5456a5c58a979b8ea9fb1b00bd854fa505afefd4f3d7731ee9b0712`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:microProfile`

```console
$ docker pull websphere-liberty@sha256:97a77c1e77968cf4a4fafcb620c2ab9e09ccd2cdb60e92396cb2e1d35a797060
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:microProfile` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197380607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7abec48ebe57cbf4e4495838c390e90dc1900b669ae7d33cec198441b6a6d`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
# Thu, 04 May 2017 23:40:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:40:39 GMT
COPY file:85a1543c7ae96e8459a3ecdbc26e3041e476ac27a7895e24ea438f07dd0552f7 in /config/ 
# Thu, 04 May 2017 23:41:00 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/     && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi     && installUtility install --acceptLicense       appSecurity-2.0 localConnector-1.0 ssl-1.0 microProfile-1.0 transportSecurity-1.0     && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi     && rm -rf /output/workarea /output/logs
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7a5bc57a434bf5dd4eb5abde3991279ab82e0cc0ddc0fb9763a5379d892ef`  
		Last Modified: Thu, 04 May 2017 23:45:03 GMT  
		Size: 534.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9882b3f040ab107b2f17da17c5e5bab6a024a727f52e09c08433fe228864de46`  
		Last Modified: Thu, 04 May 2017 23:45:05 GMT  
		Size: 24.6 MB (24606736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:webProfile6`

```console
$ docker pull websphere-liberty@sha256:f44641a80b1a43697d1c68ebf869e3f68588c8a3f870b82d57d8cd92a9a6a538
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:webProfile6` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227348842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7876a844b04fea9a9567e55aa906b7d93ae73bc4daf91cfe1d8bd3cbe73ed7`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
# Thu, 04 May 2017 23:40:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:41:19 GMT
COPY file:88c06b07fb79e4006fd1fb7042780d25c5940fd4da63eb5d18144d89ae77aa37 in /config/ 
# Thu, 04 May 2017 23:41:55 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/     && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi     && installUtility install --acceptLicense     collectiveMember-1.0 monitor-1.0 webCache-1.0 ldapRegistry-3.0 appSecurity-2.0 localConnector-1.0 restConnector-1.0 ssl-1.0 sessionDatabase-1.0     appSecurity-1.0 blueprint-1.0 concurrent-1.0 oauth-2.0 osgiConsole-1.0 serverStatus-1.0 wab-1.0 timedOperations-1.0     webProfile-6.0     && if [ ! -z $REPOSITORIES_PROPERTIES ] ; then rm /opt/ibm/wlp/etc/repositories.properties; fi     && rm -rf /output/workarea /output/logs
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340847521697639e9d977efac69469b7fc00884ea2dda7123a3bb41503302940`  
		Last Modified: Thu, 04 May 2017 23:45:30 GMT  
		Size: 535.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b72dcc3b407d3869d47ea6e756dd8f12e888a71477ceff2dbc245bc5830a36`  
		Last Modified: Thu, 04 May 2017 23:45:34 GMT  
		Size: 54.6 MB (54574970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:webProfile7`

```console
$ docker pull websphere-liberty@sha256:ae4ad2af4041926a956516513645797c84e8d12ab9f2d0a56525e3c7ce84fcbf
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:webProfile7` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235777754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2184903e8b5469fb4d40b8b89e719b3f8617a3ec2b3e64446ba8dd1521273e33`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
# Thu, 04 May 2017 23:40:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:42:13 GMT
COPY file:8a7d2385caf8e280c085cfcfad69edf89d8b4815d0f898897aa5053f0081bf61 in /config/ 
# Thu, 04 May 2017 23:42:56 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then     mkdir /opt/ibm/wlp/etc/     echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties;   fi   && installUtility install --acceptLicense     appSecurity-2.0 bluemixUtility-1.0 collectiveMember-1.0 ldapRegistry-3.0     localConnector-1.0 microProfile-1.0 monitor-1.0 restConnector-1.0     requestTiming-1.0 restConnector-2.0 sessionDatabase-1.0 ssl-1.0 transportSecurity-1.0     webCache-1.0 webProfile-7.0   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f58849d78666c612ce4e8d1273603c9263d2af29863ca7d058cabad8d96fcc`  
		Last Modified: Thu, 04 May 2017 23:45:58 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b800736ca77e9c6392cfae341f99de9f4d4257d997b0b46d33e6a1eb935aa1`  
		Last Modified: Thu, 04 May 2017 23:46:04 GMT  
		Size: 63.0 MB (63003885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:javaee7`

```console
$ docker pull websphere-liberty@sha256:cd10ceab54cd3d9bb7e9f9ef022c7e3d75b043d5ef50581faf3726358732ac80
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:javaee7` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273977214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9fec6d74969c7da582ed850bb64e00889c65fea66ff190f6bf74af6b56ecd1`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
# Thu, 04 May 2017 23:40:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:42:13 GMT
COPY file:8a7d2385caf8e280c085cfcfad69edf89d8b4815d0f898897aa5053f0081bf61 in /config/ 
# Thu, 04 May 2017 23:42:56 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then     mkdir /opt/ibm/wlp/etc/     echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties;   fi   && installUtility install --acceptLicense     appSecurity-2.0 bluemixUtility-1.0 collectiveMember-1.0 ldapRegistry-3.0     localConnector-1.0 microProfile-1.0 monitor-1.0 restConnector-1.0     requestTiming-1.0 restConnector-2.0 sessionDatabase-1.0 ssl-1.0 transportSecurity-1.0     webCache-1.0 webProfile-7.0   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs
# Thu, 04 May 2017 23:43:14 GMT
COPY file:a6a1a88d3f0473f85596df9cf7599a22f32111deb67c95183a9a45b654d347eb in /config/ 
# Thu, 04 May 2017 23:43:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:43:43 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi     && installUtility install --acceptLicense appSecurityClient-1.0 javaee-7.0 javaeeClient-7.0     && if [ ! -z $REPOSITORIES_PROPERTIES ] ; then rm /opt/ibm/wlp/etc/repositories.properties; fi     && rm -rf /output/workarea /output/logs
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f58849d78666c612ce4e8d1273603c9263d2af29863ca7d058cabad8d96fcc`  
		Last Modified: Thu, 04 May 2017 23:45:58 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b800736ca77e9c6392cfae341f99de9f4d4257d997b0b46d33e6a1eb935aa1`  
		Last Modified: Thu, 04 May 2017 23:46:04 GMT  
		Size: 63.0 MB (63003885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e305ffa6da9180315cf475da297381d83ad47ff1ca8ce28eb122508838d421`  
		Last Modified: Thu, 04 May 2017 23:46:30 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c74a2792737c460f7440b723a63491ed5ce6d6fc4946d64867a377d9d466c2`  
		Last Modified: Thu, 04 May 2017 23:46:32 GMT  
		Size: 38.2 MB (38198562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:cd10ceab54cd3d9bb7e9f9ef022c7e3d75b043d5ef50581faf3726358732ac80
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273977214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9fec6d74969c7da582ed850bb64e00889c65fea66ff190f6bf74af6b56ecd1`
-	Default Command: `["\/opt\/ibm\/docker\/docker-server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:59 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@davidcurrie)
# Thu, 04 May 2017 23:40:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:40:08 GMT
ENV LIBERTY_VERSION=17.0.0_01
# Thu, 04 May 2017 23:40:09 GMT
ARG LIBERTY_URL
# Thu, 04 May 2017 23:40:10 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 May 2017 23:40:13 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip
# Thu, 04 May 2017 23:40:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:40:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:40:18 GMT
COPY file:53b1bf224098174489129fdc8fec40f8eb4b3d0bf09e3028796a285d9a3457f1 in /opt/ibm/docker/ 
# Thu, 04 May 2017 23:40:19 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:40:19 GMT
CMD ["/opt/ibm/docker/docker-server" "run" "defaultServer"]
# Thu, 04 May 2017 23:40:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:42:13 GMT
COPY file:8a7d2385caf8e280c085cfcfad69edf89d8b4815d0f898897aa5053f0081bf61 in /config/ 
# Thu, 04 May 2017 23:42:56 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then     mkdir /opt/ibm/wlp/etc/     echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties;   fi   && installUtility install --acceptLicense     appSecurity-2.0 bluemixUtility-1.0 collectiveMember-1.0 ldapRegistry-3.0     localConnector-1.0 microProfile-1.0 monitor-1.0 restConnector-1.0     requestTiming-1.0 restConnector-2.0 sessionDatabase-1.0 ssl-1.0 transportSecurity-1.0     webCache-1.0 webProfile-7.0   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs
# Thu, 04 May 2017 23:43:14 GMT
COPY file:a6a1a88d3f0473f85596df9cf7599a22f32111deb67c95183a9a45b654d347eb in /config/ 
# Thu, 04 May 2017 23:43:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 04 May 2017 23:43:43 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi     && installUtility install --acceptLicense appSecurityClient-1.0 javaee-7.0 javaeeClient-7.0     && if [ ! -z $REPOSITORIES_PROPERTIES ] ; then rm /opt/ibm/wlp/etc/repositories.properties; fi     && rm -rf /output/workarea /output/logs
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37f1dee8914c861f3109d9eba8d976acac44e2dc710a5131f5c29672b3fdcc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 269.2 KB (269248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17669c7c6fab2f39a3f63eb8b54ae3908ff886164e909805b4d2ee4b7c30ebc`  
		Last Modified: Thu, 04 May 2017 23:44:38 GMT  
		Size: 11.7 MB (11749681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad2e7121c1b997c2d1e6ee4832823fc6465f4895c6a800b98db30e9a44f000`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966274f2b4c048bf37e9c0186ea512d25369055e50005410a0559edb03c9875`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0950ccfc325154d19e49e52830aa88d6de7afa2904a551e8970ea52679cd06`  
		Last Modified: Thu, 04 May 2017 23:44:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f58849d78666c612ce4e8d1273603c9263d2af29863ca7d058cabad8d96fcc`  
		Last Modified: Thu, 04 May 2017 23:45:58 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b800736ca77e9c6392cfae341f99de9f4d4257d997b0b46d33e6a1eb935aa1`  
		Last Modified: Thu, 04 May 2017 23:46:04 GMT  
		Size: 63.0 MB (63003885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e305ffa6da9180315cf475da297381d83ad47ff1ca8ce28eb122508838d421`  
		Last Modified: Thu, 04 May 2017 23:46:30 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c74a2792737c460f7440b723a63491ed5ce6d6fc4946d64867a377d9d466c2`  
		Last Modified: Thu, 04 May 2017 23:46:32 GMT  
		Size: 38.2 MB (38198562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:f640fd2793c9ea23a1c3bac42299afe892cdfa30c86ed9f71b177bd0f2e6a0fe
```

-	Platforms:
	-	linux; amd64

### `websphere-liberty:beta` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240591463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32824735fa234e14979b62001d5a9a207418e42f116296a84293f05f28319c39`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

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
# Tue, 25 Apr 2017 00:05:46 GMT
MAINTAINER Dinakar Guniguntala <dinakar.g@in.ibm.com> (@dinogun)
# Tue, 25 Apr 2017 00:05:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 22:30:32 GMT
ENV JAVA_VERSION=1.8.0_sr4fp5
# Thu, 04 May 2017 22:31:07 GMT
RUN ESUM="187f67fa0fa23416811aa76df70d9e43ce75bb18bba0e7be080eb83f0c21fb20"     && BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/"     && YML_FILE="jre/linux/x86_64/index.yml"     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml $BASE_URL/$YML_FILE     && JAVA_URL=$(cat /tmp/index.yml | sed -n '/'$JAVA_VERSION'/{n;p}' | sed -n 's/\s*uri:\s//p' | tr -d '\r')     && wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin $JAVA_URL     && echo "$ESUM  /tmp/ibm-java.bin" | sha256sum -c -     && echo "INSTALLER_UI=silent" > /tmp/response.properties     && echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties     && echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties     && mkdir -p /opt/ibm     && chmod +x /tmp/ibm-java.bin     && /tmp/ibm-java.bin -i silent -f /tmp/response.properties     && rm -f /tmp/response.properties     && rm -f /tmp/index.yml     && rm -f /tmp/ibm-java.bin
# Thu, 04 May 2017 22:31:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:15 GMT
MAINTAINER David Currie <david_currie@uk.ibm.com> (@dcurrie)
# Thu, 04 May 2017 23:39:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2017 23:39:26 GMT
ENV LIBERTY_VERSION=2017.4.0_0
# Thu, 04 May 2017 23:39:34 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip
# Thu, 04 May 2017 23:39:35 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2017 23:39:35 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 04 May 2017 23:39:37 GMT
RUN mkdir /logs     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config
# Thu, 04 May 2017 23:39:38 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 May 2017 23:39:39 GMT
COPY file:889efe2fa762acb1292377f98c0f0fb54c169e3f4bbab602322ba3b63ff3b3ca in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 04 May 2017 23:39:40 GMT
EXPOSE 9080/tcp 9443/tcp
# Thu, 04 May 2017 23:39:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
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
	-	`sha256:d56020343345d1c18959a22ff99361fb266de10932136b50fe1f6efccc68d675`  
		Last Modified: Tue, 25 Apr 2017 18:15:21 GMT  
		Size: 3.1 MB (3070209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa9f339d99e6b1455073ad46901f33711369c89a1540c5a30a1b6c8a06d6942`  
		Last Modified: Thu, 04 May 2017 22:35:01 GMT  
		Size: 110.9 MB (110887739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347df6828be4bf00483614ef72b97b910133f40c5e69fb9c07ed54296dda2b07`  
		Last Modified: Thu, 04 May 2017 23:44:05 GMT  
		Size: 269.3 KB (269265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d20dad33c8c5bcdab5f3e13d4adbafa244b17d6f2ac32ca741f87fa9bf901f5`  
		Last Modified: Thu, 04 May 2017 23:44:11 GMT  
		Size: 79.6 MB (79566459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566722a6c35262e6d7bfa8b3206be7463571594bcb7d6019f4e32456d5efd8ea`  
		Last Modified: Thu, 04 May 2017 23:44:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615a4ac85cd8ad3689aa52d6fff8cc4dfbbec228e23de800f7454a67a5a62c45`  
		Last Modified: Thu, 04 May 2017 23:44:05 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129bff842820b5de1cc650afaff7c1131fe5844f30a0ab9b1f473fd8a6c758ba`  
		Last Modified: Thu, 04 May 2017 23:44:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
