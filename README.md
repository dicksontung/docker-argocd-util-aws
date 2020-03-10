Use to backup argocd hosted on AWS EKS

https://hub.docker.com/r/dixont/aws-argocd

```shell script
docker run \
  -v ~/.aws:/home/argocd/.aws \
  -v ~/.kube:/home/argocd/.kube \
  --rm dixont/aws-argocd \
  argocd-util -n argocd export > backup.yaml
```

