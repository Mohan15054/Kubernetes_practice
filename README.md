## Create replicaset of nginxdemos 5 copies, capture it's ip, curl them, show screen shots 

## Steps:
    * kubectl apply -f Task-2.yml
    * kubectl get pods -l app=nginxdemos -n mohan -o wide
    * curl IP:80

![alt text](image.png)


## Notes- To curl all ip loop:

`PODS=$(kubectl get pods -l app=nginxdemos -n mohan -o=jsonpath='{.items[*].status.podIP}')

for POD in $PODS; do

 curl $POD

done`