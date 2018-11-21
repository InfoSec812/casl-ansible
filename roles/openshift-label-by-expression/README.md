# Apply a given label to OpenShift objects based on a name pattern

## Example:
```yaml
---
- hosts: localhost

  roles:
    - role: openshift-label-by-expression
      vars:
        target_namespace: labs-ci-cd      ## Apply this to ONLY objects in the specified namespace
        name_pattern: ".*selenium.*"      ## Regex patterns are supported
        label: 'app=selenium'             ## The label to be applied
```