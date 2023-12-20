+++
title = "Task 2"
weight = 20
# tags = ["observability", "tls", "database"]
+++

## Simple app with a database

### Level 1

1. Deploy a database instance of your choice
1. Add connectivity to the database from the application
    1. Expose database version under additional http endpoint (e.g. /db)

### Level 2

1. Enable telemetry for the application
    1. Expose uptime
    1. Expose number of requests processed (excluding the ones from probes)
    1. Expose the application outside the cluster via https
1. Implement database operational practices
    1. Ensure it is backed up automatically
    1. Ensure backups are stored on a separate volume or some object storage (e.g. S3 bucket or similar)
    1. Ensure there are at least two instances of the database (e.g. in the active/active or active/passive mode)
    1. Ensure the database exposes metrics compatible with the Prometheus format
