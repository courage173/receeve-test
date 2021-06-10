# running the project

Before the project is run the following env variables have to be set:
rename the `example.env` file to `.env` on the root project folder

```
MAIL_GUN_SIGNING_KEY=''
REGION=''
DYNAMODB_LOCAL_STAGE=''
DYNAMODB_ACCESS_KEY_ID=''
DYNAMODB_SECRET_ACCESS_KEY=''
DYNAMODB_LOCAL_ENDPOINT=''
DYNAMODB_REGION=''
SNS_TOPIC_ARN=''
SNS_AWS_ACCESS_KEY=''
SNS_AWS_SECRETE_KEY=''
SNS_AWS_REGION=''
```

### `Locally`

To run the project locally you have to do the following:

- Set the `DYNAMODB_LOCAL_STAGE` to dev e.g `DYNAMODB_LOCAL_STAGE=dev` to use the local DynamoDb is one is installed
- If you are running a local dynamoDB ensure you set the `DYNAMODB_LOCAL_ENDPOINT` to point to your local dynamoDb
- Set your mailgun signing key `MAIL_GUN_SIGNING_KEY` on the env file.

```sh
on project root directory run
npm start
```

### `Deploying to AWS`

Deploying the application is pretty straight forward.

- Ensure you have the AWS Cli installed and configured with the right permissions
- Set the `DYNAMODB_LOCAL_STAGE` to prod e.g `DYNAMODB_LOCAL_STAGE=prod`

```sh
on the project root directory run
npm run deploy
```
