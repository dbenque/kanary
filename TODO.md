# List of actions to be discuss and/or coded

## Validation service/deployment (simple)
Validate that the selector of the service in the spec is really selecting the pods created by the deploymentTemplate.

## Extend to more than one service (complex + discussion)
A pod can be addressed by multiple service.
Should we propose to list the servicename, or list the trafficSpec, or just propose to create a different KanaryDeployment for each service? (last proposition already possible today)

## SourceFilter based on istio (complex)
Pilot Source and traffic split using istio from the TrafficSpec (not only mirror)

## Validation based on annotation (simple)
Add annotationWatch (just like labelWatch)

## Use Controller Cache
In many places in the reconcile loop we get the deployment... maybe we can reuse the controller cache in some cases?