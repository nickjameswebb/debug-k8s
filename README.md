# debug-k8s

A container to quickly execute on a k8s cluster for debugging purposes.

## What's in it?

Based on ubuntu, contains:

- kubectl
- kapp
- git
- vim
- tree
- wget

## Commands

```
export IMAGE="<registry>/debug-k8s"

docker build . -t "$IMAGE"
docker push "$IMAGE"
kubectl run debug-k8s --image="$IMAGE" -i --tty -- /bin/bash
```