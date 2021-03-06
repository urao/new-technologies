### Cheat sheet to run useful istioctl commands 
  
1. Below are some of the istioctl useful commands
```
istioctl version
istioctl pc listener reviews-v1-59fd8b965b-xzshn 
istioctl pc listener reviews-v1-59fd8b965b-xzshn -o json
istioctl pc listener reviews-v1-59fd8b965b-xzshn --address 172.17.0.23 --port 9080 -o json
istioctl pc listener reviews-v1-59fd8b965b-xzshn --address 0.0.0.0 --port 15001 -o json
istioctl pc endpoint reviews-v1-59fd8b965b-xzshn --address 172.17.0.23 --port 9080 -o json
istioctl proxy-status
istioctl authn tls-check -n default productpage-v1-8554d58bff-dctjr
istioctl pc cluster details-v1-74f858558f-wq8dq -o json
istioctl pc cluster reviews-v1-59fd8b965b-xzshn --fqdn reviews.default.svc.cluster.local --direction inbound -o json
istioctl proxy-config routes productpage-v1-8554d58bff-dctjr --name 9080 -o json
istioctl kube-inject -f samples/sleep/sleep.yaml | kubectl apply -f -
```

## Reference
[Command List](https://istio.io)
