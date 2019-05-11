# Delivery Pipeline

We depend on compilers, databases, programming languages, package management systems, installers, and other critical programs for our daily activities. Using an automated setup helps us to reduce the time spent in installing all required dependencies for any project. Also, because the setup is standardized, new team members are able to quickly join a project without wasting time re-configuring their machine.

## Staging

Staging is the environment where we deploy every delivery. It's a testing environment, upon which developers and clients validate the work done so far. We can deploy several times per day and per week following the motto from Extreme Programming — if it hurts, do it more often. Our [Style Guide](./style-guide) process guarantees the quality of the code and the [CI/CD](./continuous-integration-continuous-delivery) process is responsible for deploying the code, running the test suite and notify the team if the build was successful or not.

This environment must be similar as possible to the production environment for providing a good level of confidence.

## Production

In production, we can find the last validated delivery, live to real users, with a scalable environment based on the service's requirements. Based on the strategy agreed with the client, we deploy the changes and features the client wants to release to the public, and we [monitor](./performance-monitoring) the current performance and [errors](./error-tracking) from the application and sub-systems. After this step and if no emergency fixes are discovered, our delivery is finally approved.

If you want to know more about this topic, there is a lovely book called [Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation](https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912).