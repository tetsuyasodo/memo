```
$ oc get secret/default-dockercfg-m2zg2 -o json | jq -r .data.".dockercfg" | base64 -d
```
