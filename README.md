# The-serverless-setup
Setup your entire infrastructure with serverless functions

## Architecture

![arch](https://user-images.githubusercontent.com/8342133/28838067-b93eda3e-770c-11e7-88fd-82dda1b53af6.png)


## Comparision:

| Features/Options |        Serverless           |        Apex         |      Chalice          |       Zappa      |      SAM   |
| -----------------|:---------------------------:|:-------------------:|:---------------------:|:----------------:|:-----------:|
|Language Written  |Nodejs | Go | Python| Python | Python|
|Functions Support |Lambda,Google,Azure,Openwhisk | AWS Lambda | AWS Lambda| AWS Lambda| AWS Lambda  |
|Provisioning      | CloudFormation| Terraform | Cloudformation |Cloudformation|YML/JSON Based Template |



## Use Cases

Benefits of Serverless Framework:

* Based on NodeJS
* CloudFormation Based Template
* Multiple Cloud Provider Support
* High Extensiblity of new features and options
 

## Setup

* Setup Authentication:

Using your AWS Credentials set up the id's at 

````
$ sudo vi ~/.aws/credentials
````
Using your GCP Credentials set up the id's at

````
$ sudo cat /home/$USER/.gcloud/keyfile.json
````
* Running latest nodjs and npm

Make sure to run latest version of nodejs and npm by running the below command:

````
$ sudo npm cache clean -f
$ sudo npm install -g n
$ sudo n stable

$ sudo ln -sf /usr/local/n/versions/node/<VERSION>/bin/node /usr/bin/nodejs
````

### Serverless Framework

#### Google Cloud Functions

Using google cloud functions can be currently implemented using Serverless framework.

### Apex

Using the apex framework is easy and simple:

### SAM

SAM denotes for Serverless Application Model.You can use the below commands for packaging and deploying a yaml based cloudformation template:

````
$ aws cloudformation package \
    --template-file /path_to_template/template.yaml \
    --s3-bucket bucket-name \
    --output-template-file packaged-template.yaml
````

For Deploying on AWS:

````
$ aws cloudformation deploy \
    --template-file /path_to_template/packaged-template.yaml \
    --stack-name my-new-stack \
    --capabilities CAPABILITY_IAM
````



## License

MIT License
