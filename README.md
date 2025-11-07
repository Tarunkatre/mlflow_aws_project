### MLFLOW on AWS

## Setup:

1. Login to AWS console.
2. Create IAM user with Administrator Access.
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a S3 Bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine

```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipend install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

### Then set aws credentials
aws configure

#final
mlflow server -h 0.0.0.0 --default-arctifact-root s3://mlflow-buc23

#open public IPv4 DNS to the port 5000

#set uri in your local terminal and in your code
export MLFLOW_TRACKING_URI = http://ec2-44-201-179-129.compute-1.amazonaws.com:5000/
```
