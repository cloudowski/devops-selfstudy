+++
title = "Task 5"
weight = 50
# tags = ["observability", "tls", "database"]
+++

## Run the app in the cloud

### Level 1

1. Provision a database as a service on the chosen cloud provider
   1. Set up replication
   1. Set up backups
1. Build a virtual machine image with the app
   1. The application can run inside a container or as standalone Linux service (systemd)
   1. The application should start when the VM starts
1. Run the app in multiple instances
   1. Use the created VM image to run the app
   1. Ensure that the number of VM instances can be changed in any time
   1. Ensure that access to the application is handled by a load balancer service configured in the cloud

### Level 2

1. Prepare code to create an environment in the cloud
   1. Ensure the code can be used to update the application after new version of the VM image is created
   2. All components except the database should be managed with code

### Level 3

1. Add an additional, cloud-specific feature to the application
   1. Create a bucket on the object storage service and upload there a simple webpage (`index.html` with a basic *“Hello Cloud!”* message)
   1. At the start of the VM download the index.html file and save in a directory that makes the page accessible from the outside
   1. Ensure that the content of the downloaded website can be displayed in the `/cloudpage` path.
1. Create and automated pipeline that builds a new VM image when a new commit is pushed to the application’s git repository
   1. Add a deployment step that also triggers a deployment to the cloud using the previously created code
