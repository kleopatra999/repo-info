## `traefik:morbier`

```console
$ docker pull traefik@sha256:9e3c89bb72a696fe1908281dc4e99fe9ad827ff7c13776da47d031f25ad963d2
```

-	Platforms:
	-	linux; amd64

### `traefik:morbier` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11781582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20298e16e9e64eec82f8f52bd0d77eab13070b55d2d45304b09dd90931885e20`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 15 Dec 2016 17:54:02 GMT
COPY file:d8282341d1fb7d2cc3d5d3523d0d4126066cc1ba8abe3f0047a459b3a63a5653 in /etc/ssl/certs/ 
# Thu, 13 Apr 2017 20:25:30 GMT
COPY file:ec7cf8cbb3faa3fb0d60458bbd5995a898484ccabed446f8b10e6f925dd2cead in / 
# Thu, 13 Apr 2017 20:25:31 GMT
EXPOSE 80/tcp
# Thu, 13 Apr 2017 20:25:32 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Apr 2017 20:25:33 GMT
LABEL org.label-schema.vendor=Containous org.label-schema.url=https://traefik.io org.label-schema.name=Traefik org.label-schema.description=A modern reverse-proxy org.label-schema.version=v1.2.3 org.label-schema.docker.schema-version=1.0
```

-	Layers:
	-	`sha256:03a84e30597f6e498aa09e940b69f623d31c22909fa05c7132e1b142f9439e38`  
		Last Modified: Thu, 15 Dec 2016 17:54:23 GMT  
		Size: 156.1 KB (156143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552885dcbedcf57c6649e7a25d4863b85e6fc160cff2eaace983f91038bed3ec`  
		Last Modified: Thu, 13 Apr 2017 20:26:23 GMT  
		Size: 11.6 MB (11625439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
