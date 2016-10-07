1. Error: **Classpath entry /home/pingping/Documents/JavaLibs/json-simple-1.1.1.jar** will not be exported or published. Runtime ClassNotFoundExceptions may result.   
2. Reason: When generating a web application, we need to take extra care with the **Referenced Libraries**.  
3. Solution:  
3.1 Install Eclipse for Java EE.  
Cons: Not recommended. 
3.2 Add Maven Plugin to fix this problem: adding dependency into war file.
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

