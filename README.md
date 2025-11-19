# ranger-plugin

# Installation
1. Move `ranger-hive-plugin-2.4.1-SNAPSHOT.jar` to `/opt/hive/lib` or other appropriate place
2. Update `hive-site.xml`
   ```
    <property>
      <name>hive.metastore.pre.event.listeners</name>
      <value>org.apache.ranger.authorization.hive.authorizer.RangerHiveMetastoreAuthorizer</value>
    </property>
   
    <property>
      <name>ranger.plugin.hive.service.name</name>
      <value><your-service-name></value>
    </property>
   ```
3. Update `ranger-hive-security.xml`
   ```
   <property>
     <name>ranger.plugin.hive.service.name</name>
     <value>hive_hms</value>
   </property>

   <property>
     <name>ranger.plugin.hive.policy.source.impl</name>
     <value>org.apache.ranger.admin.client.RangerAdminRESTClient</value>
   </property>

   <property>
     <name>ranger.plugin.hive.policy.rest.url</name>
     <value>http://ranger:6080</value>
   </property>
   ```   
