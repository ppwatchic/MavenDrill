## Problem Description
In my pom.xml, there is maven coordinate
```
<dependency>
			<groupId>org.hamcrest</groupId>
			<artifactId>hamcrest-library</artifactId>
			<version>1.3</version>
			<scope>test</scope>
		</dependency>
```
Maven failed to install the file automatically. 

## Solution
After the many trials, the only one helps me is the following command line: 
```
mvn install:install-file -Dfile=D:\JavaLibs\hamcrest-all-1.3.jar 
-DgroupId=org.portletfacesorg.hamcrest -DartifactId=hamcrest-library
-Dversion=1.3 -Dpackaging=jar -DgeneratePom=true
```
It works because the file path has to include the jar file name. 





## Reference 
1. [Maven install:install-file](http://sravanmodugula.blogspot.com/2010/09/maven-installinstall-file-access-is.html).
