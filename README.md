# Developer Desktop Configurator
There are Ansible playbooks which help to configure developers environment for Magento dev

Run MySQL inside Docker

```
docker run -d -p 3306:3306 --restart always -e MYSQL_PASS="admin" --name mysql tutum/mysql
```
