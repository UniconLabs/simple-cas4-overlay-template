simple-cas4-overlay-template
============================

Generic CAS maven war overlay to exercise the latest versions of CAS 4.x line

This overlay could be freely used as a starting template for local CAS maven war overlays.

# Versions
```xml
<cas.version>4.0.1</cas.version>
```

# Recommended Requirements
* JDK 1.7+
* Apache Maven 3+
* Servlet container supporting Servlet 3+ spec (e.g. Apache Tomcat 7+)

# Configuration
The `etc` directory contains the sample configuration files that would need to be copied to an external file system location (`/etc/cas` by default)
and configured to satisfy local CAS installation needs. Current files are:

* `cas.properties`
* `log4j.xml`

# Deployment

* Execute `mvn clean package`
* Deploy resultant `target/cas.war` to a Servlet container of choice
