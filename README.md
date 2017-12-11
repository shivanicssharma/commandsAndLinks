# commandsAndLinks
Commands and Links

Build a Secure SPA With Spring Boot and OAuth
https://dzone.com/articles/build-a-secure-spa-with-spring-boot-and-oauth?edition=343094&utm_source=Weekly%20Digest&utm_medium=email&utm_campaign=Weekly%20Digest%202017-12-06


For generating java classes from json or json schema; Add following plugin into pom.xml

Change the sourceType to JSON Schema if using schema instead of json.

<plugin>
				 <groupId>org.jsonschema2pojo</groupId>
				 <artifactId>jsonschema2pojo-maven-plugin</artifactId>
				 <version>0.4.34</version>
				 <configuration>
				 <sourceDirectory>${project.basedir}/src/main/resources/schema</sourceDirectory>
				 <targetPackage>com.ca.sso.policydata.api.fed.objects</targetPackage>
				 <useCommonsLang3>true</useCommonsLang3>
				 <sourceType>JSON</sourceType>
				 </configuration>
				 <executions>
				 <execution>
				 <goals>
				 <goal>generate</goal>
				 </goals>
				 </execution>
				 </executions>
	</plugin>
  
  Add the json files into /src/main/resources/schema directory.
  
  Run the maven build with goal generate-sources.
  
  mvn generate-sources
