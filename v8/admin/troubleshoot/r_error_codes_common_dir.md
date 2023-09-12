# Common directory integration service error messages {#r_error_codes_common_dir .reference}

Use the codes included in the error messages generated by HCL Connections™ to identify problems with the common directory integration service and find their solutions.

## Common directory integration service messages { .section}

|Message|Cause|Solution|
|-------|-----|--------|
|CLFRK0002E: Unable to determine memberUUID for \{0\}.|The federated realm is not configured correctly or the wimconfig.xml file contains errors.|Follow the instructions provided in the Installation Guide for [Setting up federated repositories](../install/t_inst_federated_repositories.md). If you edited the wimconfig.xml file, revert to the original copy of the file.|
|CLFRK0003E: ID for '\{0\}' is not available|The directory cannot find user profile data from backend services such as LDAP or the Profiles database, perhaps because the records have been deleted.|1.  Identify the missing records and make sure they are available in the backend services: either LDAP or the Profiles database. <br> 2.  Resynchronize the records based on an email or login attribute value key for all of the services.|
|CLFRK0004E: Unable to locate LDAP Profile Service \{0\}.|The LDAP component is not functioning properly.|You may be trying to implement a configuration that is not currently supported by HCL Connections. To prevent this error, you would have to configure the system as a 'standalone LDAP user registry,' which is currently not supported.|
|CLFRK0005E: Unable to locate Persona Profile Service \{0\}.|The Profiles Service Atom feed component is not functioning properly.|You may be trying to implement a configuration that is not currently supported by HCL Connections. To prevent this error, you would have to configure the system to rely on the Profiles service Atom feed, which is not currently supported.|
|CLFRK0006E: Unable to locate Memory Profile Service \{0\}.|The memory model service of the Waltz component is not functioning properly.|You may be trying to implement a configuration that is not currently supported by HCL Connections. To prevent this error, you would have to configure Tomcat as the memory model, which is an unsupported configuration.|
|CLFRK0007E: Unable to access directory settings for HCL Connections \{0\}.|HCL Connections cannot find the LotusConnection-config.xml file.|Make sure the LotusConnection-config.xml file is installed on the system.|

**Parent topic:**[Error message reference](../troubleshoot/c_error_codes.md)
