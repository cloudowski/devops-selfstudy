+++
title = "Task 3"
weight = 30
# tags = ["observability", "tls", "database"]
+++

## Make the app (more) secure

### Level 1

1. Deploy HashiCorp Vault
    1. Deploy outside or inside the cluster
    1. Store the database password in Vault and make it accessible directly to the app (i.e bypassing the creation of a Secret object)
1. Gather the metrics from the app - set up proper metrics & monitoring system

### Level 2

1. Use the dynamic database secrets feature instead of static (KV) engine
1. Create a dashboard with the metrics from the app
    1. Include the number of ready/running replicas
    1. Include the number of requests
1. Ensure that the cluster is monitored and the necessary notifications are configured.
1. Set up monitoring for the app
    1. Send an email notification when there are fewer than 3 ready instances
    1. Send an email notification when there is a Pod in Pending or CrashLoopbackOff state for more than 3 minutes

### Level 3

1. Ensure logs from the cluster and apps are stored and can be viewed
1. Ensure that cluster events are archived and can be viewed
