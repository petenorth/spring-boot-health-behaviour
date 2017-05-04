# spring-boot-health-behaviour

This projects a behaviour of spring boot and health checks.

Run 

    mvn spring-boot:run
    
Then in another terminal run

    curl -v http://localhost:8081/health
    
The JSON output should indicate that that the application is down since it was not possible to connect to an ActiveMQ instance.

BUT the spring-boot:run application has started successfully and there is no information indicating that anything is wrong.

