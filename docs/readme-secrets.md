# Examples of the encrypted secrets files in this repo

## Common
`deployments/[name]/secrets` has the following files:
prod.yaml and staging.yaml
```
pangeo:
  jupyterhub:
    proxy:
      secretToken: XXXXX
    auth:
      type: github
      github:
        clientId: XXXXXXX
        clientSecret: XXXXXXXXX
        callbackUrl: "https://nasa.pangeo.io/hub/oauth_callback"
```
there are separate oauth keys and secret tokens for staging and prod


## AWS
`deployments/nasa/secrets` has the following files:

aws-confg.txt
```
[default]
region=us-east-1
aws_access_key_id=XXXXXXXXXXXX
aws_secret_access_key=XXXXXXXXXXXXXXXXXX
```
where these keys are for an iam user or role that circleci assumes when deploying


## Google
`deployments/dev/secrets` has the following files:

gcloud-service-key.json 
```
{
"type": "service_account",
"project_id": "XXXXXXX",
"private_key_id": "XXXXXXXX",
"private_key": "-----BEGIN PRIVATE KEY-----\XXXXXXX\n-----END PRIVATE KEY-----\n",
"client_email": "XXXXXXXXX",
"client_id": "XXXXXX",
"auth_uri": "https://accounts.google.com/o/oauth2/auth",
"token_uri": "https://oauth2.googleapis.com/token",
"auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
"client_x509_cert_url": XXXXXX
}
```

## Azure
