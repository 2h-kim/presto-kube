# Presto on kubernetes

## Purpose
- Study presto on kubernetes
- The kubernetes test was performed on docker-desktop context.

## Test environment
- window 11
- docker : Docker version 20.10.17, build 100c701
- docker-compose : docker-compose version 1.29.2, build 5becea4c
- presto : 0.276.1
- kubectl : v1.24.2
- helm : v3.10.0

## docker repo
- ocker repo is on personal docker repositories : `kgg6008/presto:20220924`
- docker image is build by presto-cluster repo : [link](https://github.com/2h-kim/presto-cluster)

## run
```bash
helm install -g .
```

### show
```bash
kubectl get svc | grep presto 
kubectl get svc | findstr presto # window
```
to connect local port
```bash
kubectl port-forward svc/chart-1664014133-presto-kube 8080:8080 # 8080 to 8080
```