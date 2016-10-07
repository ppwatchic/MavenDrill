## Maven Configuration Problem

1. Error: **org.codehaus.plexus.archiver.jar.Manifest.write(java.io.PrintWriter)	pom.xml	/WebAppDemo	line 1**.
2. Environment:   
2.1 Maven Plugin:
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
2.2 Eclipse version:  
Version: 2.2.0.v20160606-1100  
Build id: I20160606-1100  
2.3 m2e: 
1.7.0.20160603-1933  
3. Cause of error: the maven-war-plugin.  
4. Solution: 


