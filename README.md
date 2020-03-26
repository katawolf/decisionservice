# Decision service

Service back for the decision handle<br />
This service is deployed with cloud run on [https://decisionservice.katawolf.jtutzo.fr](https://decisionservice.katawolf.jtutzo.fr)

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### `yarn test`

Launches the test runner.

### `yarn test:watch`

Launches the test runner in the interactive watch mode.

### `yarn build`

Builds the app for production to the `dist` folder.<br />

## Deployment management on kubernetes cluster

### With `kubectl`

First build your app and create a docker image.

`docker build -t jtutzo/katawolf/decisionservice .`

Push docker image on your repository.

`docker push jtutzo/katawolf/decisionservice`

Deploy app on your kubernetes cluster.

`kubectl apply -f ./k8s`

After for remove app on your kubernetes cluster.

`kubectl delete -f ./k8s`

### With `skaffold`

Build and deploy on your kubernetes cluster.

`skaffold run`

After for remove app on your kubernetes cluster.

`skaffold delete`
