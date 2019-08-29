## AWS CLI

01.    `curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"` (downloads AWS bundle, requires python and pip)
02.    `unzip awscli-bundle.zip` (unzips AWS)
03.    `sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws` (installs bundle)
04.    `aws configure --profile user` (sets up access key ID, secret access key, aws region and output format defaults for using AWS CLI)
05.    `aws ec2 describe-instances --profile user-name` (shows you config profile for a given user on a given AWS service, ec2 in this example)
06.    `aws iam upload-server-certificate --server-certificate-name STAR_example_com --certificate-body file://STAR_example_com.crt --private-key file://star_example_com.pem --certificate-chain file://ca-chain-amazon.crt --path /cloudfront/*/` (uploads an SSL certificate to AWS IAM service)
07.    `aws iam update-server-certificate` (updates AWS IAM SSL certificates)
08.    `aws iam get-server-certificate --server-certificate-name STAR_example_com` (gets you the details of a current SSL certificate)