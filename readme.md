# The Apollo Project

This fork updates Scala from 2.10 to 2.11. I wanted to embed Apollo for
integration tests but different Scala versions can't exist in the same JVM.
This is difficult because old versions of third-party dependencies don't
have Scala 2.11 artifacts, and the artifacts which were built for 2.11
are not backwards compatible.

STOMP and REST APIs work but other features may not. Some tests may not pass.

## Building the Source Code

Prerequisites:

* [Maven >= 3.0.2](http://maven.apache.org/download.html)
* [JDK 1.6 or 1.7](http://java.sun.com/javase/downloads/widget/jdk6.jsp)

Then run:

    mvn clean install -DskipTests
    
This will build the binary distribution and place them in the
`apollo-distro/target` directory.


