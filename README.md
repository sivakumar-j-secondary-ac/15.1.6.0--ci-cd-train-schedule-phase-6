#Auto scaling

```
git clone https://github.com/kubernetes-incubator/metrics-server.git
cd metrics-server/
git checkout ed0663b3b4ddbfab5afea166dfd68c677930d22e
kubectl create -f deploy/1.8+/
kubectl get --raw /apis/metrics.k8s.io/
cd ~/
git clone https://github.com/sivakumar-j-secondary-ac/15.1.5.0--ci-cd-train-schedule-phase-5.git
cd cicd-pipeline-train-schedule-autoscaling/
cat > train-schedule-kube.yml
---paste the contents from master branch train-schedule-kube.yml file
kubectl apply -f train-schedule-kube.yml

Increase CPU by /generate-cpu-load or by the below busybox image commands

kubectl run -i --tty load-generator --image=busybox /bin/sh
while true; do wget -q -O- http://<kubernetes node public ip>:8080/generate-cpu-load; done

```

# Watch the hpa as it unfolds

```
kubectl get hpa -w 
```
