# Status

Undone: 


## Read this please

Logic: 
First using the {{ firsttime_connect_user }} credentials, keypair is generated 
The tasks in host provisioning will be done using {{ firsttime_connect_user }} 
For running subsequent nfs or k8 tasks, user can then ssh using the ansible user created 

## NFS and k8s

Don't forget to change hostnames in inventory file

### NFS

To configure NFS server change variable ```flag_nfs_server``` in inventory to ```true``` 
To configure NFS client change variable ```flag_nfs_client``` in inventory to ```true``` 

Usage: 
```
ansible-playbook nfs.yml
```

### k8s

To configure persistent volume change variable ```flag_k8s_create_sc in inventory``` to ```false``` and start playbook with:
```
ansible-playbook k8s_sc.yml
```

### Ansible module for k8s

In order to use k8s module for ansible install in first from galaxy:
```
ansible-galaxy collection install kubernetes.core
```