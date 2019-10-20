1. Create ECR Repo: demo/python-batch-job
2. Run Docker commands

```
cd job
$(aws ecr get-login --no-include-email --region us-west-2)
docker build .
docker run 122f277f62d4
docker tag 122f277f62d4 python-batch-job:latest
docker tag python-batch-job:latest 100000000000.dkr.ecr.us-west-2.amazonaws.com/demo/python-batch-job:latest
docker push 100000000000.dkr.ecr.us-west-2.amazonaws.com/demo/python-batch-job:latest
```
