# In Kube master

cd ~/
git clone https://github.com/kubernetes-incubator/metrics-server.git
cd metrics-server/
git checkout ed0663b3b4ddbfab5afea166dfd68c677930d22e
kubectl create -f deploy/1.8+/
kubectl get --raw /apis/metrics.k8s.io/
cd ~/
git clone https://github.com/sivakumar-j-secondary-ac/15.1.6.0--ci-cd-train-schedule-phase-6.git
cd cicd-pipeline-train-schedule-autoscaling/
vi train-schedule-kube.yml
kubectl apply -f train-schedule-kube.yml
