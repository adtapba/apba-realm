# Bundle containing a realm to be used by APBA bundles

It makes available a JAAS properties login module. When deployed, it creates a file named usersapba.properties on the etc directory of Apache ServiceMix 6.0.0, which contains users, groups and roles.

### Karaf installation command

`bundle:install -s mvn:es.apba.infra.esb.support/apba-realm/1.0.0-SNAPSHOT`

### Sample use on Karaf
```
jaas:realm-manage --realm apba

jaas:user-add aismanager_adminuser test1234

jaas:group-add aismanager_adminuser GROUP_AISMANAGER_ADMIN_USERS

jaas:group-role-add GROUP_AISMANAGER_ADMIN_USERS ROLE_AISMANAGER_PUBLISHERS
jaas:group-role-add GROUP_AISMANAGER_ADMIN_USERS ROLE_AISMANAGER_PROXY_SERVICES_ADMIN_USERS

jaas:update
```
