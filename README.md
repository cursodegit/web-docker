# Stack para despliegue de cursodegit.com

Este repositorio contiene el stack para desplegar la web de cursodegit.com en producción usando Docker Swarm.

## Despliegue

```bash 
> git clone https://github.com/cursodegit/web-docker.git
> cd web-docker
> touch acme.json
> chmod 666 acme.json
> docker stack deploy -c docker-compose.yml cursodegit
```

## SSL

La gestión de SSL se está haciendo a través de CloudFlare. Por ello dentro de traefik se ha configurado
el `entryPoint` a través del puerto 80.

