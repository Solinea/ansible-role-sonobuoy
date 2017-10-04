# ansible-role-sonobuoy

This role installs Heptio's [sonobuoy](https://github.com/heptio/sonobuoy) for the purpose of conducting a 'smoke test' of a k8s environment.

Sonobuoy will gather *a lot* of data. But the only data we query for the smoke test is the final result of the end-to-end test. That is found in the e2e log here:
```commandline
      sonobuoy/results/plugins/e2e/results/e2e.log
```

If the test result is a failure, query this log for additional information to explain the failure.

Example usage:
```yaml
- hosts: kube-master[0]
  gather_facts: false
  roles:
    - { role: sonobuoy }

```

