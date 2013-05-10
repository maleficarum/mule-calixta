mule-calixta
=============

This connector is a very basic way to send SMS using calixta service.

Introduction
============

To include this connector in your project, you have to include mule-calixta jar.

After that, you must modify mule-config.xml to add the connector schema as follows :

#### Add the namespaces
	xmlns:calixta="http://www.mulesoft.org/schema/mule/calixta"

#### Include de XSD location
	http://www.mulesoft.org/schema/mule/calixta http://www.mulesoft.org/schema/mule/calixta/1.0-SNAPSHOT/mule-calixta.xsd

#### Configuration
=============

To send single SMS:

	<calixta:send destination="NUMBER" text="The SMS body" />

To send SMS's to multiple destinations:

	<calixta:send destination="NUMBER1,NUMBER2" text="The SMS body" />


#### Maven integration
=============

Include maleficarum mvn repo :

<repository>
        <id>maleficarum</id>
        <url>https://raw.github.com/maleficarum/maven/master/</url>
        <releases>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
        </releases>
    </repository>

Add dependency :

        <dependency>
            <groupId>mx.maleficarum</groupId>
            <artifactId>mule-calixta</artifactId>
            <version>1.0-SNAPSHOT</version>
        </dependency>
