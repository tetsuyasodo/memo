```
[sodo@dsgw02 ~]$ oc rsh pod/elasticsearch-cdm-v7iju121-1-5f8f9b6b7b-wl8v7
Defaulting container name to elasticsearch.
Use 'oc describe pod/elasticsearch-cdm-v7iju121-1-5f8f9b6b7b-wl8v7 -n openshift-logging' to see all of the containers in this pod.


sh-4.2$
secret_dir=/etc/elasticsearch/secret/
curl -k -s  --cacert $secret_dir/admin-ca \
      --cert $secret_dir/admin-cert \
      --key  $secret_dir/admin-key \
      -H Content-type:application/json \
https://localhost:9200/_cat/indices


green open audit-000001           i5TPByjySxuljcbCkZxxqw 3 1       0 0  1.5kb   783b
green open .kibana_92668751_admin lPEY1kU8SNiwoeATyzDNWA 3 1       2 0 38.5kb 19.2kb
green open .security              S7I17OenSyKw792ISFhPqA 1 1       5 0 59.9kb 29.9kb
green open infra-000001           rKkCvxS2RFuGZ3QlTWbNVw 3 1 2407345 0  2.3gb  1.1gb
green open app-000001             VFTU4q-EQKGjPvaFibssjw 3 1       0 0  1.5kb   783b
green open .kibana_1              pk7FzSE7T0ekQ2yujbvOOA 1 1       1 0  7.7kb  3.8kb
sh-4.2$
```
