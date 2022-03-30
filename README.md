# Terrarium Deployment Utilities

A repo for Terrarium Deployment Utilities such as Helm charts and Terraform modules

## Deployment

1. Clone this repo and ensure you are authenticated with the cluster you want to deploy to
1. Create a `secretValues.yml` and populate it with the following content substituting your values

```
aws_access_key_id: <BASE64_ENCODED_ACCESS_KEY_ID>
aws_access_key_secret: <BASE64_ENCODED_ACCESS_KEY_SECRET>
aws_region: <BASE64_ENCODED_AWS_REGION>
imagePullSecret: <BASE64_ENCODED_DOCKER_SECRET>
modules_service:
  bucket_name: <MODULES_BUCKET_NAME>
```

1. Execute `helm install terrarium . -f secretValues.yml`