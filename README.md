# Migration to the Cloud with Containerisation
#####

docker login -u AWS -p $(aws ecr get-authorization-token  --region us-east-1 --output text --query 'authorizationData[].authorizationToken' | base64 --decode | cut -c 5- ) 992382761454.dkr.ecr.us-east-1.amazonaws.com

992382761454.dkr.ecr.us-east-1.amazonaws.com
