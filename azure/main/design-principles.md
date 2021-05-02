* `Design for self healing`
    * Retry failed operations
    * Protect failing remote services (Circuit Breaker)
    * Isolate critical resources (Bulkhead)
    * Perform load leveling (Queue based)
    * Failover (always run multiple instances)
    * Compensate failed transactions (avoid distributed transactions)
    * Checkpoint long-running transactions
    * Degrade gracefully (e.g. recommendation system failure shouldn't affect anything else)
    * Throttle clients (slow down clients that create excessive load, use quotas)
    * Block bad actors
    * Use leader election (If the coordinator fails, a new one selected, e.g. zookeeper)
    * Test with fault injection (usually only success path is tested)
    * Embrace chaos engineering (randomly inject failures in production)
* `Make all things redundant` (no single points of failure)
    * Consider business requirements (cost and complexity must be justified)
    * Place VMs behind a load balancer (distributes traffic to healthy VMs)
    * Replicate databases
    * Partition for availability (failure in one shard will have limited impact)
    * Deploy to more than one region
* `Minimize coordination` (to achieve scalability)
    * Embrace eventual consistency (e.g. via Compensating Transaction)
    * Use domain events to synchronize state (Interested services can listen for the events)
    * CQRS and event sourcing (Reduce contention between read workloads and write workloads)
    * Partition data (don't put all your data in one schema)
    * Design idempotent operations (e.g. via queue)
    * Use asynchronous parallel processing
    * Use optimistic concurrency (DB validates transaction after a commit)
    * Parallel, distributed algorithms (e.g. MapReduce)
* `Design to scale out` (horizontally)
    * Avoid instance stickiness (same request always goes to the same instance)
    * Identify bottlenecks (e.g. backend database)
    * Offload resource-intensive tasks (run them as background jobs)
    * Design for scale in (when instances get removed)
