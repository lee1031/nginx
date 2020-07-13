# Nginx Brotli Docker Image

[![Build Status](https://travis-ci.org/lee1031/nginx.svg?branch=master)](https://travis-ci.org/lee1031/nginx)
[![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/lee1031/nginx)

## Supported branches 
- 1.16: `1.16.1`
- 1.17: `1.17.10`、`1.17.9`
- 1.19: `1.19.1`、`1.19.0`

## Getting image

```sh
docker pull lee1031/nginx
```

## nginx.conf

```conf 
load_module  modules/ngx_http_brotli_filter_module.so;
load_module  modules/ngx_http_brotli_static_module.so;

user  nginx;
worker_processes  auto;

error_log  /var/log/nginx/error.log warn;
pid        /var/run/nginx.pid;

events {
  ...
}

http {
  ...
}
```
