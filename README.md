This project combines

* [Netty] (http://netty.io/)
* [Jersey] (http://jersey.java.net/)
* [JAXB (Java Architecture for XML Binding)](http://www.oracle.com/technetwork/articles/javase/index-140168.html)
* [JSON] (http://www.ietf.org/rfc/rfc4627.txt)

### How to

Import as Maven project in Eclipse. Run the `JaxrsServer`. The first argument defines the port, which is 9999 by default.

* [http://localhost:9999/users/1] (http://localhost:9999/users/1)
  * Should return an empty list: `[]`
* [http://localhost:9999/users/2] (http://localhost:9999/users/2)
  * Should return a list with an user: `[{"userId":100,"username":"test"}]`

### Known bugs

`mvn package` produces a package with dependencies under `target`: `Jersey-Netty-Container-Example-0.0.1-SNAPSHOT.jar`

Calling a ressource on the jar results in the following exception:

```
Caused by: com.sun.jersey.api.MessageException: A message body writer for Java class java.util.ArrayList, and Java type java.util.List<de.dennis_boldt.User>, and MIME media type application/json was not found
```
### Thanks to

* [Gabriel Ciuloaica] (https://github.com/devsprint/jersey-netty-container)
