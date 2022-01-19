# trivy-plugin-webhook
A [Trivy](https://github.com/aquasecurity/trivy) plugin that scans the images of a kubernetes resource

## Install

```
$ trivy plugin install github.com/aquasecurity/trivy-plugin-webhook
$ trivy webhook -h
Usage: trivy webhook [-h,--help] TYPE NAME [TRIVY OPTION]
 A Trivy plugin that scans the images of a kubernetes resource.

Options:
  -h, --help    Show usage.

Examples:
  # Scan a Pod
  trivy webhook pod mypod

  # Scan a Deployment
  trivy webhook deployment mydeployment -n mynamespace

  # Scan a Job and filter by severity
  trivy webhook job myjob -n mynamespace -- --severity CRITICAL
```

## Usage
Trivy's options need to be passed after `--`.

```
# Scan a Pod
$ trivy webhook pod mypod

# Scan a Deployment
$ trivy webhook deployment mydeployment -n mynamespace

# Scan a Job and filter by severity
$ trivy webhook job myjob -n mynamespace -- --severity CRITICAL
```

