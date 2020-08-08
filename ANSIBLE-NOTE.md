Ansible note
- check ansible version:
```
ansible --version
```

- check ansible location
```
which ansible
```

- Command to run ansible play book
```
ansible-playbook -i hosts demoplays.yaml
```

- notify is the tag that use to notify handler when change happened in ansible
- changed_when is the tag that use to setting task always result in change
```
 - name: inginx config
     debug:
        msg: "put nginx config in place"
     notify: restart nginx
```
```
handlers:
 - name: restart nginx
     debug:
       msg: "service nginx restart"
```
