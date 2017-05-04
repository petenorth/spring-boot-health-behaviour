# spring-boot-health-behaviour

This projects a behaviour of spring boot and health checks.

Run 

    mvn spring-boot:run
    
Then in another terminal run

    curl -v http://localhost:8081/health
    
The JSON output should indicate that that the application is down since it was not possible to connect to an ActiveMQ instance.

BUT the spring-boot:run application has started successfully and there is no information indicating that anything is wrong.

To deploy to Openshift follow

./README_orig.md

I believe that this describes a deployment that sets up liveness and readiness checks, the readiness check will fail (because it can't connect to ActiveMQ) but there will be no information within the logs to say why it has failed other than the readiness check failing.
