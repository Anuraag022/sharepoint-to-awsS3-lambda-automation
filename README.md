# sharepoint-to-awsS3-lambda-automation

This exercise uses a python script that pulls files from a Sharepoint location on to a S3 bucket. This is turn is automated using a Lambda Trigger through the way of setting up of a Lambda Function which in turn sets up the System Variables. Attaching codes for the same.

The following diagram should give a concise understanding of how the flow will be  -  


<img width="514" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/fd419795-0d45-43ac-a6a6-b0621dcd0225">



<img width="258" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/3da2cae0-5380-4f2e-8733-73ef5e262b55">

The lambda_handler is the function that aws looks to execute. By defualt in aws it is 'lambda_handler' function which helps in nomenclature is kept the same. 

AWS_ACCESS_KEY_ID = os.environ['aws_access_key']
To extract System variables

<img width="380" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/05df78fa-386c-426f-af21-de2f54928013">

Variables that will come from the system and will be set against the objects

<img width="427" alt="image" src="https://github.com/Anuraag022/sharepoint-to-awsS3-lambda-automation/assets/9040716/02e99e83-2099-4dcc-8b11-6e64b93daac3">

Credentials to download files from

packages to install - 
boto3 to connect to awsS3
Office365-REST-Python-Client to interact with sharepoint

How to get the 'requirements' and push it to aws to be run as a packge-
Open Terminal > 

create venv

pip freeze > requirements.txt

pip install --target ./package -r requirements.txt (packs all packages & dependencies and pushes to 'package')

cd package/

--will have to zip this folder to push as, download the zip.exe to use its functionalities in terminal. Download from - http://stahlworks.com/tool-zipunzip

"C:\Program Files\zip.exe" --will show all the functions within zip.exe

-- We are in the mail folder and now we push all the files in the folder to 'deployment-package-zip' '-r' is recursion which pushes files one by one

"C:\Program Files\zip.exe" -r ../deployment-package.zip .

--also need to move lambda_function.py to the above zip file hence

"C:\Program Files\zip.exe" -g deployment-package.zip lambda_function.py


