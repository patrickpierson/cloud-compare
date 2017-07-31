### AWS

Create S3 bucket 

> $ aws s3 mb s3://webdev-webtech

Deploy JavaScript to S3 and make it public 

> $ aws s3 sync ./_site s3://webdev-webtech --acl public-read

http://webdev-webtech.s3.amazonaws.com/index.html

### Azure

Create a deployment user

> $ az webapp deployment user set --user-name webdevtesting --password REDACTED

Create a resource group

> $ az group create --name myResourceGroup --location eastus2

Create an Azure App Service plan

> $ az appservice plan create --name myAppServicePlan --resource-group myResourceGroup --sku FREE

Create a web app

> $ az webapp create --name webdev --resource-group myResourceGroup --plan myAppServicePlan

### Google

Make Bucket

> gsutil mb gs://webdevdemo

Deploy JavaScript to Google

> gsutil rsync -R ./ gs://webdevdemo

Make it public

> gsutil acl ch -u AllUsers:R gs://webdevdemo


