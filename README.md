# AWS API

This repo contains a SAM application showing how to integrate using infrastructure-as-code (IaC). You can use this to help develop your own project quickly. This specific application is intended to show an application which allows a mobile device to write a single devices current, allow end users to get all devices current locations, and allow end users to get a single devices location history. The information information is stored in an Amazon Aurora RDS database with a read replica and standby replica, and uses VPC endpointss to allow communication to the Secrets Manager, Systems Manager Parameter Store, and CloudWatch services. We will also be using the KMS key for encryption and decryption using a customer managed key. This specific solution uses AWS Lambda to allow developers to focus on business logic without so much infrastructure managment (scaling for example).

Important: this application uses various AWS services and there are costs associated with these services after the Free Tier usage - please see the [AWS Pricing page](https://aws.amazon.com/pricing/) for details. You are responsible for any AWS costs incurred. No warranty is implied in this example.

## Requirements

* AWS CLI already configured with Administrator permission
* Python 3.8

## Deployment Instructions

1. [Create an AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) if you do not already have one and login.

1. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [install the AWS Serverless Application Model CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) on your local machine.

1. Create a new directory and navigate to that directory in a terminal.

1. Clone this repo:

```
git clone https://github.com/tim-pugh/awsAPI
cd awsAPI
sam build
sam deploy --guided
sam delete <stack name>
```

1. When finished please run the following command to delete the stack:

```
sam delete <stack name>
```
----

SPDX-License-Identifier: GNU GENERAL PUBLIC LICENSE v3
