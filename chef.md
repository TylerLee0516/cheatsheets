```
knife node list
knife node show <node_name>

knife bootstrap --sudo -x $(whoami) -N <host_name> <node_name>
knife node run_list add <node_name> 'role[<role_name>]'
knife node environment_set <NODE_NAME> <ENVIRONMENT_NAME>
knife tag create <NODE_NAME> <TAG_NAME>
```
