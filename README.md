# zk8

# Troubleshooting services

1. First, make sure you’re connecting to the service’s cluster IP from within the
   cluster, not from the outside.

2. Don’t bother pinging the service IP to figure out if the service is accessible
   (remember, the service’s cluster IP is a virtual IP and pinging it will never work).

3. If you’ve defined a readiness probe, make sure it’s succeeding; otherwise the
   pod won’t be part of the service.
   
4. To confirm that a pod is part of the service, examine the corresponding End-
   points object with kubectl get endpoints .
   
5. If you’re trying to access the service through its FQDN or a part of it (for exam-
   ple, myservice.mynamespace.svc.cluster.local or myservice.mynamespace) and
   it doesn’t work, see if you can access it using its cluster IP instead of the FQDN.
   
6. Check whether you’re connecting to the port exposed by the service and not
   the target port.
   
7. Try connecting to the pod IP directly to confirm your pod is accepting connec-
   tions on the correct port.
   
8. If you can’t even access your app through the pod’s IP, make sure your app isn’t
   only binding to localhost.