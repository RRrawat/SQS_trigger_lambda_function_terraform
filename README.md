# Terrsform-SQS-to-trigger-lambda-example
Example for how to create a AWS Lambda triggered by Amazon Simple Queue Service (SQS) in Terraform.

$ terraform apply
$ aws sqs send-message --queue-url $(terraform output sqs_url) --message-body "hello, world"

# Verifying the Setup
1. Log into AWS and go to the SQS console
2. Select your queue
3. On the bottom go to the Lambda Triggers tab
4. You should see the ARN of your Lambda function with an Enabled Status
5. Go to the Lambda console
6. Select your Lambda function
7. You should see SQS as a Trigger attached to your lambda.

![image](https://user-images.githubusercontent.com/81628422/139830402-c2508982-97c4-41b8-8ec9-6872715032fe.png)
