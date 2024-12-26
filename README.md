# redisrole

```bash
ansible-playbook -i inventory.ini redis_playbook.yml -e "redis_version=6.2.6"
```




## install redis without makeing roles in ubuntu/debian by using the below commands

**1** 
```bash
ansible localhost -m apt -a "name=redis-server state=present" --become
```
**2**
```bash
ansible localhost -m service -a "name=redis-server state=started enabled=yes" --become
```
**3**
```bash
ansible localhost -m apt -a "name=redis-server state=present" --become && ansible localhost -m service -a "name=redis-server state=started enabled=yes" --become
```
