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

### Comparison
* [Service matrix](https://github.com/open-guides/og-aws#service-matrix)
    * AWS vs Google Cloud vs Azure vs Openstack vs BYO (Open source)
* 
