# ansible-role-sonobuoy

Example usage:
```yaml
- hosts: kube-master[0]
  gather_facts: false
  roles:
    - { role: sonobuoy }

```
