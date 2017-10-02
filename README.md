# WatchThis! API
The following api is created using the following serverless AWS Platform to build it:

        -Lambda & API Gateway for our serverless API
        -DynamoDB for our database
        -Cognito for user authentication and securing our APIs

Based on the [Serverless Stack](http://serverless-stack.com) in order to create a full-stack serverless applications.
This repo is for the serverless backend API that I built over the course of the tutorial in order to learn more about the framework
#### Usage

To use this repo locally you need to have the [Serverless framework](https://serverless.com) installed.

``` bash
$ npm install serverless -g
```

Clone this repo and install the NPM packages.

``` bash
$ git clone https://github.com/mouryam/watchthis-app-api.git
$ npm install
```

Run a single API on local.

``` bash
$ serverless webpack invoke --function list --path event.json
```

Where, `event.json` contains the request event info and looks something like this.

``` json
{
  "requestContext": {
    "authorizer": {
      "claims": {
        "sub": "USER-SUB-1234"
      }
    }
  }
}
```

Finally, run this to deploy to your AWS account.

``` bash
$ serverless deploy
```

#### Maintainers
The following API for WatchThis! app is maintained by Mourya Meda. Send me an [email][Email] if you have any questions.

[Email]: mailto:medamourya@gmail.com
