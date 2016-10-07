Problems when using `mvn package` to generate a war file.

**1.1 Error: No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?**  
**1.2 Solution: Declare m in `pom.xml` as following:**
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
**2.1 Error: Unable to locate the Javac Compiler in: /usr/local/java/jre1.8.0_101/../lib/tools.jar**  
**2.2 Solution:** go to Windows->Preferences->Java->Installed JREs->(clicked on the installed JREs)->Edit->JRE name = JAVA_HOME.  
**3.1 Error: Tests in error:There are test failures.**  
**3.2 Reason: didn't fulfill the test case in the implementation.**  
**3.3 Solution: **  
**4.0**In .settings there is file `org.eclipse.wst.common.project.facet.core.xm.` with origin setting:
```
<?xml version="1.0" encoding="UTF-8"?>
<faceted-project>
  <installed facet="cloudfoundry.standalone.app" version="1.0"/>
</faceted-project>
```
Now change it: <installed facet="jst.web" version="3.0"/>. 



