+++
title = "Task 1"
weight = 10
# tags = ["container", "replicas", "registry"]
+++

## Start - simple web application

### Level 1

1. Create a simple web application in the language of your choice (e.g. Go, Python) that just displays a hostname and the app version
1. Create a container image definition in a Dockerfile
Use advanced techniques if applicable (e.g. multistage, build from “scratch”)
    1. Make it as small as possible
    1. Ensure the image is available for both amd64 and arm64 architectures
    1. Publish the image in a private registry
1. Run the application on the cluster in multiple instances
    1. Don’t forget about best practices (probes, resources requests/limits)

### Level 2

1. Automate the build process
    1. Ensure that after each push to the git repository with the application’s source a build process starts and publish the image
    1. Make sure the image doesn’t have critical vulnerabilities after each build

