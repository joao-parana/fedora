# fedora

```
git clone git@github.com:joao-parana/fedora.git
cd fedora
docker build -t parana/systemd_rawhide .
cd httpd
docker build -t parana/myhttpd .
docker run --privileged -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 80:80 parana/myhttpd
```

