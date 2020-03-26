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

## Deploy on kubernetes cluster with `kubectl`

### `docker build -t jtutzo/katawolf/decisionservice .`

Builds app and create a docker image.

### `docker push jtutzo/katawolf/decisionservice`

Pushes image on repository

### `kubectl apply -f ./k8s-manifests`

Deploys app on kubernetes cluster.

### `kubectl delete -f ./k8s-manifests`

Deletes app on kubernetes cluster.

## Deploy on kubernetes cluster with `skaffold`

### `skaffold run`

Builds and deploys app on kubernetes cluster.
