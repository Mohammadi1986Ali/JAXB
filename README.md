# JAXB
JAXB (Java Architecture for XML Binding) provides:
- Marshal (write) Java objects into XML
- Unmarshal (read) XML into objects

These dependencies should be added when using JDK9+
When using JDK11 the version of maven-jaxb2-plugin will be 0.14.0

    <dependencies>
        <dependency>
            <groupId>javax.xml.bind</groupId>
            <artifactId>jaxb-api</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
        <dependency>
            <groupId>com.sun.xml.bind</groupId>
            <artifactId>jaxb-core</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
        <dependency>
            <groupId>com.sun.xml.bind</groupId>
            <artifactId>jaxb-impl</artifactId>
            <version>${jaxb.version}</version>
        </dependency>
    </dependencies>

We can use both:
- maven-jaxb2-plugin (uses the JAXB reference implementation by Oracle/Sun)
- jaxb2-maven-plugin (uses Apache Xerces)