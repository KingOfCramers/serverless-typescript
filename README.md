# Basic Serverless & Typescript configuration

This project is a template for creating serverless, Lambda functions on AWS quickly.

The functions are written in Typescript. For information about loading the `.env` files, head [here](https://www.serverless.com/plugins/serverless-dotenv-plugin).

## Installation

`yarn install`

## Development

To spin up the development server locally, run `yarn dev`

This is an alias for the `serverless offline` command which uses the serverless-offline plugin to spin up a development server with our lambdas at various endpoints.

The functions can then be hit with Postman, Curl, or another service.

To run a function in isolation use the `yarn local` command, followed by the function name. This is an alias for `serverless invoke local --function`

To run the same function on the cloud, after deployment, use `yarn cloud`

## Deployment

`yarn deploy`

This command set the `NODE_ENV` to production, loading the correct environment variables, and then deploys the function to the cloud (configuration inside the `serverless.ts` file).
