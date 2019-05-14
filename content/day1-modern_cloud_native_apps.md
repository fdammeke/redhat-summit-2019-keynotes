## Modern cloud-native app development
--
### AMQ instead of REST
* AMQ based service mesh based on QPID instead of REST API
* Something to think about: How to address network latency?
* Each microservice can have it's own database type
--
### Istio
* Envoy sidecar container
* Data plan & control plane
* Intra microservice transaction
* Gateway solution that provides API to outside world
* Canary roll-out to impact only a small subset of customers
* Direct traffic based on browser client / logged on / ..
* kiali add-on to visualise service graphs
--
## Functions and serverless
* knative
  * knative-build = s2i (source to image)
* small and start as fast as possible
--
## Go faster
* Don't invent hot water
* Re-use what already exists
* Even if it's cloud based
  * Check build-in cloud based services
  * SaaS/DBaaS/SSO/Infinispan/Notification-as-a-service/..
--
The original slides are available [online](https://bit.ly/cloudnative2019).
