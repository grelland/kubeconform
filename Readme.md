# Kubeconform

[![Build status](https://github.com/yannh/kubeconform/workflows/build/badge.svg?branch=master)](https://github.com/yannh/kubeconform/actions?query=branch%3Amaster)
[![Go Report card](https://goreportcard.com/badge/github.com/yannh/kubeconform)](https://goreportcard.com/report/github.com/yannh/kubeconform)

Kubeconform is a Kubernetes manifests validation tool. Build it into your CI to validate your Kubernetes
configuration using the schemas from the registry maintained by the
[kubernetes-json-schema](https://github.com/instrumenta/kubernetes-json-schema) project!

It is inspired by and similar to [Kubeval](https://github.com/instrumenta/kubeval), but with the
following improvements:
 * **high performance**: will validate & download manifests over multiple routines
 * support for **Kubernetes CRDs**

### Usage

```
$ ./bin/kubeconform -h
Usage of ./bin/kubeconform:
  -dir value
        directory to validate (can be specified multiple times)
  -file value
        file to validate (can be specified multiple times)
  -k8sversion string
        version of Kubernetes to test against (default "1.18.0")
  -n int
        number of routines to run in parallel (default 4)
  -output string
        output format - text, json (default "text")
  -schema value
        file containing an additional Schema (can be specified multiple times)
  -skip string
        comma-separated list of kinds to ignore
  -strict
        disallow additional properties not in schema
  -summary
        print a summary at the end
  -verbose
        print results for all resources
```

### Credits

 * @garethr for the [Kubeval](https://github.com/instrumenta/kubeval) and
 [kubernetes-json-schema](https://github.com/instrumenta/kubernetes-json-schema) projects
