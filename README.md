# hello-spark-k8s

Experiments to get spark running in a kubernetes context

## Quickstart

```
curl -s "https://get.sdkman.io" | bash
sdk install java 8.0.275-amzn
sdk install sbt

brew install kubectl apache-spark
```

```bash
kubectl apply -f spark8s.yml

kubectl scale deployment.apps/spark-worker --replicas=4

kubectl port-forward service/spark-driver 8080:8080

# Open a browser with http://localhost:8080
# Ctrl-C on the terminal to exit the port forwarding

kubectl delete -f spark8s.yml
```

![Screenshot of Spark UI showing 4 worker nodes](screenshot.png)

# TODO:
 - https://kienmn97.medium.com/deployment-of-standalone-spark-cluster-on-kubernetes-ba15978658bf
