# sharepoint-to-awsS3-lambda-automation

This exercise uses a python script that pulls files from a Sharepoint location on to a S3 bucket. This is turn is automated using a Lambda Trigger through the way of setting up of a Lambda Function which in turn sets up the System Variables. Attaching codes for the same.

The following diagram should give a concise understanding of how the flow will be  -  


<img width="514" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/fd419795-0d45-43ac-a6a6-b0621dcd0225">


AWS_ACCESS_KEY_ID = os.environ['aws_access_key']
The lambda_handler is the function that aws looks to execute. By defualt in aws it is 'lambda_handler' function which helps in nomenclature is kept the same. 

AWS_ACCESS_KEY_ID = os.environ['aws_access_key']
To extract System variables

AWS_ACCESS_KEY_ID = os.environ['aws_access_key']
Variables that will come from the system and will be set against the objects

<img width="427" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/02e99e83-2099-4dcc-8b11-6e64b93daac3">

Credentials to download files from

packages to install - 
boto3 to connect to awsS3
Office365-REST-Python-Client to interact with sharepoint
