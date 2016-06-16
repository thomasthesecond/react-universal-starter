### POIs

A node.js microservice for displaying POIs.

#### Installation

```shell
cp .env.example .env
npm install
```

#### Running the application

Run `npm run start` in one terminal to start the server on port 3000

You can now visit any POI by its Atlas ID http://localhost:3000/poi/372147  
You can also visit by slug http://localhost:3000/france/paris/sights/landmarks-monuments/eiffel-tower

When visiting by slug, an Elasticsearch request is made to retrieve the Atlas ID, in order to redirect to the endpoint using the Atlas ID.

#### Simulate Production Environment
Run this...

```shell
npm run build
```

Then...

```shell
NODE_ENV=production USE_LOCAL_ASSETS=true ./bin/www
```

#### Tests
There are a few NPM scripts for testing...

```shell
npm run test      # Normal testing
npm run test:ci   # Run tests and watch for changes
npm run test:cov  # Run tests with coverage
```

To see the code coverage, run `npm run test:cov`, and then `open /coverage/lcov-report/index.html`.
