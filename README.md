# Nest Cloud Run
Runs a simple nest.js api in Google Cloud Run

### Branches
All git branches are merged into master
- rock/run-in-cloud - the basic nest app running with a default controller and a process.env dump
- rock/set-env-from-deploy - set NODE_ENV to develop for local development and set it to production on Cloud Run

## Build image and deploy to Cloud Run
```bash
gcloud builds submit --tag gcr.io/[PROJECT-ID]/nest-cloud-run
```
```bash
gcloud beta run deploy --image gcr.io/[PROJECT-ID]/nest-cloud-run --platform managed
```
- To set environment variables during deployment: 
```bash
gcloud beta run deploy --image gcr.io/[PROJECT-ID]/nest-cloud-run --platform managed -update-env-vars NODE_ENV=production
```
#Nest Boilerplate Readme

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

  Nest is [MIT licensed](LICENSE).
