### Cloud
* `Cloud computing` - on-demand delivery of IT resources over the Internet (e.g. computing power, data storage)
    * The main enabling technology for cloud computing is `virtualization` (separates a physical device from virtual devices)
* Types of computing:
    * `On premises` - you manage everything
    * `IaaS` (Infrastructure as a Service) - service manages networking, storage, servers, virtualization
        * AWS, DigitalOcean, Azure, GCE
    * `PaaS` (Platform as a Service) - IaaS + service manages OS, middleware, runtime
        * AWS Elastic Beanstalk, Heroku
    * `SaaS` (Software as a Service) - PaaS + service manages data and application (service manages everything)
        * Dropbox, Salesforce
    * `Serverless` - servers are abstracted away. Not suitable for complex apps. With lots of functions interacting with one another - complexity grows very quickly.
        * `Function as a Service (FaaS)`
        *
* Goals for the state of infrastructure:
    * `Visibility` - what services you are using, how you use them. Notifications when somebody makes changes. Detection of misconfigurations and incidents
    * `Automation` - automatically scale solutions, resolve incidents, rollback to previous configurations
    * `Flexibility` - how easy it is to make changes/improve your configurations
* Interfaces:
    * `Web interface` (e.g. AWS console) use cases:
        * Read-only usage (to understand state of the system)
        * When learning new service
        * Unique tasks (e.g. run EC2 isntance, check something, throw it away)
    * `CLI` (Command Line Interface):
        * Basic way to save and automate operations 
    * `API` (Application Programming Interface):
        * Do not call `API` directly, better use `SDK` 
    * `SDK` (Software Development Kit):
        * e.g. add SDK as dependency to build.gradle, write code that launches `EC2` instances
* Best practices:
    * Package your application and all dependencies in a `Docker` image
    * Introduce random instance termination during business hours (e.g. Chaos Monkey)
### Comparison
* [Service matrix](https://github.com/open-guides/og-aws#service-matrix)
    * AWS vs Google Cloud vs Azure vs Openstack vs BYO (Open source)
* 
