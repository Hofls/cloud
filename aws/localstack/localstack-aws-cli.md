#### Getting started. CLI
* [Install & run Localstack](localstack.md)
* Install AWS CLI:
    * `apt install awscli`
    * `pip3 install --upgrade awscli`
* Configure AWS CLI:
    ```
    export AWS_ACCESS_KEY_ID="test"
    export AWS_SECRET_ACCESS_KEY="test"
    export AWS_DEFAULT_REGION="us-east-1"
    alias aws='aws --endpoint-url=http://localhost:4566'
    ```
* Make sure its working:
    * `aws dynamodb list-tables`
    * `aws apigateway get-rest-apis`
    * `aws kinesis list-streams`

#### S3
* `aws s3api create-bucket --bucket sample-bucket`
* `aws s3api list-buckets`
* `touch index.html`
* `aws s3api put-object --bucket sample-bucket --key index.html --body index.html`
* `aws s3api list-objects --bucket sample-bucket`
* `aws s3api delete-object --bucket sample-bucket --key index.html`
* `aws s3api delete-bucket --bucket sample-bucket`
