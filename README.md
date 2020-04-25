# Jflex Sample

## Files
- src/main/jflex/example.flex: the simple grammar specification
- src/test/data/test.txt: sample input

# Using Maven

##Generate the lexer
```
  mvn generate-sources
```
The jflex-maven-plugin reads the grammar src/main/jflex/example.flex and generates a Java scanner Yylex class by default.
  Expected output:
 - target/generated-sources/flex/Yylex.java.
 
 ## Package
 ```
   mvn package
 ```
 The package phase does everything above and packages the jar archive of the Java classes. You can then run
  ```
   java -jar target/jflex_sample-SNAPSHOT-1.0.jar src/test/data/test.txt(or file path)
  ```
 
 #Reference:
 Please read the document in JFlex-Maven-Plugin[https://github.com/jflex-de/jflex/blob/master/jflex/examples/simple/README.md].
  
  