# test
simple API utilizing automation and AWS best practices

OBJECTIVE
Launch a simple API utilizing automation and AWS best practices.

REQUIREMENTS
•DynamoDB table
oMust contain multiple unique records (sample structure provided below, you maydetermine your own schema as desired)
•Lambda Function
oMust be written in a language supported natively by AWS (Node.js, Java, C#, Go, Python
–NO SHIMS)
oMust log execution output to CloudWatch Logs
•API Gateway with two stages (dev and prod) exposing endpoints for the Lambda function
oMust have a path to expose all DynamoDB records as well as a single record
▪Example:
•/id should return a list of all records1
2
3
4
5
•/id/5 should return the details of record #5 in DynamoDB
{
“id”: “5”,
“details” {
“firstName”: “Onica”, “lastName”: “Test”
}
}
•CloudWatch Logs
oMust have a retention policy of 30 days
•IAM roles and policies must be created in the least permissive model (AVOID USINGAWS MANAGED POLICIES)
•All AWS resources must be created using Serverless Framework, Terraform, or CloudFormation
•No resources may be created or managed by hand other than EC2 SSH keys
