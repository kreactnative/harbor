### build arm64 base image
```
docker build -f make/photon/core/Dockerfile.base -t goharbor/harbor-core-base:dev .
docker build -f make/photon/db/Dockerfile.base -t goharbor/harbor-db-base:dev .
docker build -f make/photon/exporter/Dockerfile.base -t goharbor/harbor-exporter-base:dev .
docker build -f make/photon/jobservice/Dockerfile.base -t goharbor/harbor-jobservice-base:dev .
docker build -f make/photon/log/Dockerfile.base -t goharbor/harbor-log-base:dev .
docker build -f make/photon/nginx/Dockerfile.base -t goharbor/harbor-nginx-base:dev .
docker build -f make/photon/portal/Dockerfile.base -t goharbor/harbor-portal-base:dev .
docker build -f make/photon/prepare/Dockerfile.base -t goharbor/harbor-prepare-base:dev .
docker build -f make/photon/redis/Dockerfile.base -t goharbor/harbor-redis-base:dev .
docker build -f make/photon/registry/Dockerfile.base -t goharbor/harbor-registry-base:dev .
docker build -f make/photon/registryctl/Dockerfile.base -t goharbor/harbor-registryctl-base:dev .
docker build -f make/photon/trivy-adapter/Dockerfile.base -t goharbor/harbor-trivy-adapter-base:dev .
```
### build harbor arm64
```
make package_offline -e  VERSIONTAG=v2.12.0 PKGVERSIONTAG=v2.12.0 UIVERSIONTAG=v2.12.0  DEVFLAG=false  CLAIRFLAG=false
```