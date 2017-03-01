
Alfresco Patch to Authentication required for every API and protocol
====================================================================

Described at issue [ALF-21757](https://issues.alfresco.com/jira/browse/ALF-21757) and [ALF-21521](https://issues.alfresco.com/jira/browse/ALF-21521)

Alfreso is requiring the same authentication scheme for every API and protocol form Alfresco 5.1. Since then, configuring authentication systems like Kerberos provokes that WebDav, SSP, CMIS and REST API cannot be used, as there is no way to configure a Kerberos client auth for any of them.

This patch, restores basic authentication to access to all these other protocols and preserves default one for the rest.

**Compatibility**
The current version has been developed using Alfresco 5.1 and Alfresco SDK 2.2.0

***Original Alfresco resources have been overwritten***

Using the ready-to-deploy-plugin
--------------------------------------
The binary distribution is made of one amp file to be deployed in Alfresco as a repo module at **releases** tab.

You can install them by using standard [Alfresco deployment tools](http://docs.alfresco.com/community/tasks/dev-extensions-tutorials-simple-module-install-amp.html) in `alfresco.war`

Building the artifacts
----------------------
If you are new to Alfresco and the Alfresco Maven SDK, you should start by reading [Jeff Potts' tutorial on the subject](http://ecmarchitect.com/alfresco-developer-series-tutorials/maven-sdk/tutorial/tutorial.html).

You can build the artifacts from source code using maven
```$ mvn clean package```