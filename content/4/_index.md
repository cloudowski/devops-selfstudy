+++
title = "Task 4"
weight = 40
# tags = ["observability", "tls", "database"]
+++

## Bring even more security

### Level 1

1. Ensure that the app doesn’t run as a root user
2. The service should try to automatically fix vulnerabilities in the dependencies by creating a Pull/Merge Request

### Level 2

1. Add a scanning service for the source code of the app
1. Ensure that each Pod **MUST** in selected namespaces run a container on non-root user
1. Ensure that the traffic from and to the app is restricted
    1. Forbid traffic from other namespaces
    1. Explicitly allow traffic between the app instances and the database

### Level 3

1. Ensure that a trusted TLS certificate is used to provide the https access 
1. Minimize the syscalls used by the app with a custom syscomp profile
1. Monitor each time when someone execs into the app container and send a mail notification
1. Ensure that the whole network traffic is encrypted within the cluster
