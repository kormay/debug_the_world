# Does not have minimum availability
> ERROR: https://www.gengleiming.com:8443/ping is not accessible (Could not resolve host: www.gengleiming.com)

### 注意加上下面的hostAliases

```
"spec": { 
    "template": { 
        "spec": { 
            "hostAliases": [ 
                { 
                    "hostnames": 
                    [ 
                        "{{ rancher_server_hostname }}" 
                        ], 
                        "ip": "{{ rancher_server_ip }}"
                    }
                ]
            }
        }
    }
```

### 在spec.template.spec下，加上

```
hostAliases: [ 
    { 
        "hostnames": 
        [ 
            "{{ rancher_server_hostname }}" 
        ], 
        "ip": "{{ rancher_server_ip }}" 
    }
] 
```

### 然后保存
