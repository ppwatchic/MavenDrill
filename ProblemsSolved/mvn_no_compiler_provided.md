Problems when using `mvn package` to generate a war file.

**1. Error: No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?**  
**2. Solution 1: Declare maven-compiler-plugin in `pom.xml` as following:**
```
<build>
 <plugins>
 <!-- Set a JDK compiler level -->
  <plugin>
   <groupId>org.apache.maven.plugins</groupId>
   <artifactId>maven-compiler-plugin</artifactId>
	 <version>2.3.2</version>
		<configuration>
		 <source>${jdk.version}</source>
		 <target>${jdk.version}</target>
		</configuration>
	</plugin>
 </plugins>
</build>
```  
**3. Solution 2:** If the above doesn't work, the compiler has to be explicitly specified as below:
```
<!-- Set a JDK compiler level -->
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>				
				<configuration>
					<verbose>true</verbose>
					<fork>true</fork>
					<executable>/usr/lib/jvm/java-8-openjdk-i386/bin/javac</executable>
					<compilerVersion>1.8</compilerVersion>
				</configuration>
			</plugin>
			```  
			.




