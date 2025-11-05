# Push image to ECR
Run below commands to push our custom Grafana image to ECR.
```
aws ecr get-login-password --region eu-central-1 --profile backend-test | docker login --username AWS --password-stdin 241523129597.dkr.ecr.eu-central-1.amazonaws.com
```

```
docker build -t grafana-custom .
```

```
docker tag grafana-custom 241523129597.dkr.ecr.eu-central-1.amazonaws.com/monitoring:grafana
```

```
docker push 241523129597.dkr.ecr.eu-central-1.amazonaws.com/monitoring:grafana
```