[![unifi-controller](https://raw.githubusercontent.com/linuxserver/docker-templates/master/linuxserver.io/img/unifi-banner.png)](https://www.ubnt.com/enterprise/#unifi)

```
docker run \
  --name=unifi \
  -d \
  -e PUID=1000 \
  -e PGID=1000 \
  -e MEM_LIMIT=1024M \
  -p 3478:3478/udp \
  -p 10001:10001/udp \
  -p 8080:8080 \
  -p 8443:8443 \
  -p 1900:1900/udp \
  -p 8843:8843 \
  -p 8880:8880 \
  -p 6789:6789 \
  -p 5514:5514 \
  -v /volume1/docker/unifi:/config \
  --restart unless-stopped \
  linuxserver/unifi-controller

```
