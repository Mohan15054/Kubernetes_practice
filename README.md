### Create a pod using busy box which will print time every minute, viewable in log 

## steps:
    * kubectl apply -f Task-1.yml
    * kubectl get pods -n mohan
    * kubectl logs -n mohan task-1 -c time-printer -f
