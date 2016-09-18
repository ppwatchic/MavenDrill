1. Create project 
We go to the directory where we want to create the project, and we type these: 
```
mvn archetype:generate -DgroupId=com.pingping.firstexample 
-DartifactId=firstexample -DarchetypeArtifactId=maven-archetype-quickstart 
-DinteractiveMode=false
```
And this will create a project with source and test directoreis that include just a small unit test class and a hello world program.
A file named `pom.xml` is also generated. 

2. Build project 
To generate bytecode from java class, we type: 
`mvn package`
and we can see the results from the terminal. 
