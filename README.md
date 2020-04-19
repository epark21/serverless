# Individual Project 4
# Serverless Data Engineering Pipeline

Goals
- Reproduce the architecture of a serverless data engineering project.
- Enhance the project by extending the functionality of the NLP analysis: adding entity extraction, key phrase extraction, or some other NLP feature.

# Workflow
![Image](../master/images/20.png?raw=true)

# 1. Launch AWS Cloud9, create and configure settings for new environment
![Image](../master/images/1.png?raw=true)


# 2. Create Github repo, create ssh keys, git clone
![Image](../master/images/2.png?raw=true)
```
ssh-keygen -t rsa 
```
![Image](../master/images/3.png?raw=true)

```
git clone git@github.com:epark21/uncdocker.git
```

# 3. Create Serverless Application (Producer)
![Image](../master/images/4.png?raw=true)


# 4. Create SQS Queue
![Image](../master/images/5.png?raw=true)


# 5. Create table in DynamoDB
![Image](../master/images/6.png?raw=true)


# 6.  Deploy lambda function (Producer)
![Image](../master/images/7.png?raw=true)


# 7.  Verify deployment is successful in Lambda
![Image](../master/images/8.png?raw=true)

![Image](../master/images/9.png?raw=true)


# 8.  Add Trigger to call lambda function every minute
![Image](../master/images/10.png?raw=true)


# 9. Trigger function is running and putting messages into SQS
![Image](../master/images/11.png?raw=true)


# 10. Build Serverless Application (Consumer)
![Image](../master/images/12.png?raw=true)


# 11. Install Required Packages then Deploy
```
pip3 install boto3 --target ../
pip3 install python-json-logger --target ../
pip3 install wikipedia --target ../
pip3 install pandas --target ../
```


# 12. Verify Deployment and Add SQS Trigger to pull 10 msg 
![Image](../master/images/13.png?raw=true)


# 13. Observe Queue, CloudWatch Metrics, Logs
![Image](../master/images/14.png?raw=true)
![Image](../master/images/15.png?raw=true)
![Image](../master/images/16.png?raw=true)


# 14. Stores results in S3 Bucket
![Image](../master/images/17.png?raw=true)


# 15. Download and review results (name, Wikipedia snippet, sentiment)
![Image](../master/images/18.png?raw=true)
![Image](../master/images/19.png?raw=true)













