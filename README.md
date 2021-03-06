# serverless-email
A serverless Azure function to send emails using SendGrid. Built using serverless framework's serverless-azure-functions.

## Serverless Framework
https://github.com/serverless/serverless
## Serverless Azure Plugin
https://github.com/serverless/serverless-azure-functions

## SendGrid NodeJS Docs
https://github.com/sendgrid/sendgrid-nodejs

## Installation

Install serverless using npm

```bash
npm install serverless -g
```
Install all the dependencies
```bash
npm install
```
Rename .env.sample file to .env and plugin your SendGrid API Key.  

Finally push the function to Azure using serverless, which will ask for an authentication prompt.
```bash
serverless deploy
```

## Usage
The CLI will return you the endpoint of the deployed Azure Function  

The function endpoint is secured using Azure Function Host Key which you can find in the **App Keys** tab of your function on Azure Portal. This needs to be added to the HTTP Request

```bash
https://<APP_NAME>.azurewebsites.net/api/<FUNCTION_NAME>?code=<API_KEY>
```

You can add **recipient**, **subject** and **text** in the request body to send the email.


