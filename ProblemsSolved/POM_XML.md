## Maven Configuration Problem

1. Error: **org.codehaus.plexus.archiver.jar.Manifest.write(java.io.PrintWriter)	pom.xml	/WebAppDemo	line 1**.
2. Environment: 
1) Maven Plugin: 
```
<plugin>
			 	<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-war-plugin</artifactId>
				<version>3.0.0</version>
				<configuration>
					<archive>
						<manifest>
						<addClasspath>true</addClasspath>
						</manifest>
						</archive>
				</configuration>
</plugin>
```
