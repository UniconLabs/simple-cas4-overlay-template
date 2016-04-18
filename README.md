CAS4 Overlay Template
============================

Generic CAS maven war overlay to exercise the latest versions of CAS 4.x line. This overlay could be freely used as a starting template for local CAS maven war overlays.

# Versions
```xml
<cas.version>4.2.1</cas.version>
```

# Recommended Requirements
* JDK 1.8+

# Configuration
The `etc` directory contains the configuration files that need to be copied to `/cas/etc`.

Current files are:

* `cas.properties`
* `log4j2.xml`

# Build

```bash
mvnw clean package
```

or

```bash
mvnw.bat clean package
```

# Deployment

## Embedded Jetty

* Create a Java keystore at `/etc/cas/jetty/thekeystore` with the password `changeit`.
* Import your CAS server certificate inside this keystore.

```bash
mvnw jetty:run-forked
```

CAS will be available at:

* `http://cas.server.name:8080/cas`
* `https://cas.server.name:8443/cas`

## External
Deploy resultant `target/cas.war` to a Servlet container of choice.
