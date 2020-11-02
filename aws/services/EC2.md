### Main features:
* `Security group` - make port accessible to entire internet (e.g. 80)
* `EC2 Instance connect` - connect to instance via SSH in a browser (alternative to PuTTy)
    * Looks like it is working only with specific instances (Amazon Linux 2 AMI)
* `Auto Scaling Groups` - automatically change amount of EC2 instances, based on load
* `Snapshot` - save image (to restore data in case of loss / run new instances)
* `Placement groups` - pick "cluster" if you want instances located close to each other (for low latency)
* `Load Balancers` - send traffic to the least loaded instance

