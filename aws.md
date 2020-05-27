## AWS CLI

01.    `curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"` (downloads AWS bundle, requires python and pip)
02.    `unzip awscli-bundle.zip` (unzips AWS)
03.    `sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws` (installs bundle)
04.    `aws configure --profile user` (sets up access key ID, secret access key, aws region and output format defaults for using AWS CLI)
05.    `aws ec2 describe-instances --profile user-name` (shows you config profile for a given user on a given AWS service, ec2 in this example)
06.    `aws iam upload-server-certificate --server-certificate-name STAR_example_com --certificate-body file://STAR_example_com.crt --private-key file://star_example_com.pem --certificate-chain file://ca-chain-amazon.crt --path /cloudfront/*/` (uploads an SSL certificate to AWS IAM service)
07.    `aws iam update-server-certificate` (updates AWS IAM SSL certificates)
08.    `aws iam get-server-certificate --server-certificate-name STAR_example_com` (gets you the details of a current SSL certificate)

## AWS Lambda

01.    `aws lambda create-alias --function-name your-function-name-here --description "alias for live version of function" --function-version 1 --name your-alias-name-here` (creates an alias for your functions, so you can push new versions up easily)
02.    `aws lambda update-alias --function-name your-function-name-here --function-version 3 --name your-alias-name-here` (update alias versions of function name)


### AWS SAM CLI

01.   `sam --version` (gets version of SAM)
02.   `sam build` (downloads dependencies and runtime you need, ie. Node for JS)
03.   `sam local start-api` (sets up a local endpoint for testing an API, defaults to running on `localhost:3000`)
`sam generate-event` (mock sample payloads from event sources) 
04.   `sam package --template-file template.yaml --output-template packaged-template.yaml --s3-bucket your-bucket-here` (how to packge up a serverless function for deployment)
05.   `sam deploy --template-file packaged-template.yaml --stack-name your-stack-here --capabilities SNAKE_CASE_HERE` (moves the built package into the 'action' environment in AWS, so it's basically ready to receive invocations from events)
06.   `sam invoke` (literally invokes a Lambda function one time)
07.   `sam start-lambda` (starts the endpoint for local testing)
