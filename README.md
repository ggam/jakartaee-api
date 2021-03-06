Jakarta EE APIs
===============

This project generates the Jakarta EE API jar files and javadocs
by combining the artifacts produced by the individual API projects.

To update the version of an API that's included, update the corresponding
property in the top level pom.xml file.

To add or remove an API, all pom.xml files will need to be updated.

Note that the glassfishbuild-maven-plugin is used to create "clean"
pom.xml files to be published for each of the projects.

Building
--------

Prerequisites:

* JDK8+
* Maven 3.0.3+

Use the staging profile if necessary to pull in staged versions of artifacts.

Run the full build:

`mvn -Pstaging install javadoc:javadoc`

Locate the API jar files:
- jakartaee-api/target/jakartaee-api-{version}.jar
- jakartaee-web-api/target/jakartaee-web-api-{version}.jar

Locate the javadocs:
- jakartaee-api/target/site/apidocs
- jakartaee-web-api/target/site/apidocs

Locate the Bill Of Materials (BOM) file:
- jakartaee-bom/target/pom.xml
