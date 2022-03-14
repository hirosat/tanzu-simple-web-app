### Tanzu Community Edition Application Toolkit Sample Workload

This project is a simple spring boot web application. It was created by
visiting start.spring.io, choosing the Spring Web framework, and adding the
HelloController.

## Prerequisites

Installed Tanzu Community Edition Application Toolkit and its dependencies.

## Deploying Workload

Use the Tanzu CLI to create the Workload from the workload.yaml file. Assumes

```
tanzu apps workload create -f workload.yaml --yes
```

Watch kpack find the correct buildpack and build the workload. Look for the
"Build successful" message when complete.

```
tanzu apps workload tail tanzu-simple-web-app
```

## Testing the workload

The workload should end up deployed on knative. Test the workload:

```
curl http://tanzu-simple-web-app.default.127-0-0-1.sslip.io 
```
