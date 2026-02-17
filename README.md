# aws-stepfunctions-workflows
AWS Step Functions workflow pattern
Account Validation & Notification Workflow
Use Case - Validates user account data and conditionally writes to DynamoDB. Sends notification based on validation result.

Architecture Flow
Start
Lambda → Validate account data
Choice State → Is account valid?
If valid:
DynamoDB PutItem
SNS Publish (Success Email)
Success state
If invalid:
SNS Publish (Failure Email)
Fail state
End

Services Used
AWS Step Functions
AWS Lambda
Amazon DynamoDB
Amazon SNS
<img width="428" height="448" alt="image" src="https://github.com/user-attachments/assets/dfebd02e-bfe0-45da-bec7-e407143fa871" />

