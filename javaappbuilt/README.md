# Java Application Build ![CI status](https://img.shields.io/badge/tested-yes-brightgreen.svg)

This is a [sample Java application](https://spring.io/guides/gs/maven/) built with Apache Maven tool.

### Requirements
* Maven
* Java

## Usage

```console
$ #assuming we are in the directory the script resides in
$ bash javaappbuild
```
## Script algorithm
The script follows the following logic: 

  1) Create directory structure and source files for Java application;

  2) Check whether Apache Maven is installed and install if not;

  3) Build the Java application 

  4) Start the Java app

NB! The build log and the application's output go to STDIN
### Sample output
```console
root@kali:/home/vagrant/built_projects/builtjavaapps/javaappbuilt# bash javaappbuild 
[INFO] Scanning for projects...
[INFO] 
[INFO] --------------------< org.springframework:gs-maven >--------------------
[INFO] Building gs-maven 0.1.0
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ gs-maven ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/vagrant/built_projects/builtjavaapps/javaappbuilt/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ gs-maven ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 2 source files to /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/classes
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 1.199 s
[INFO] Finished at: 2018-08-13T04:23:51-04:00
[INFO] ------------------------------------------------------------------------
[INFO] Scanning for projects...
[INFO] 
[INFO] --------------------< org.springframework:gs-maven >--------------------
[INFO] Building gs-maven 0.1.0
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ gs-maven ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/vagrant/built_projects/builtjavaapps/javaappbuilt/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ gs-maven ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 2 source files to /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/classes
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ gs-maven ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /home/vagrant/built_projects/builtjavaapps/javaappbuilt/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.1:testCompile (default-testCompile) @ gs-maven ---
[INFO] Changes detected - recompiling the module!
[WARNING] File encoding has not been set, using platform encoding UTF-8, i.e. build is platform dependent!
[INFO] Compiling 1 source file to /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:2.12.4:test (default-test) @ gs-maven ---
[INFO] Surefire report directory: /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/surefire-reports

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running hello.GreeterTest
Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.054 sec

Results :

Tests run: 1, Failures: 0, Errors: 0, Skipped: 0

[INFO] 
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ gs-maven ---
[INFO] Building jar: /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/gs-maven-0.1.0.jar
[INFO] 
[INFO] --- maven-shade-plugin:2.1:shade (default) @ gs-maven ---
[INFO] Including joda-time:joda-time:jar:2.9.2 in the shaded jar.
[INFO] Replacing original artifact with shaded artifact.
[INFO] Replacing /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/gs-maven-0.1.0.jar with /home/vagrant/built_projects/builtjavaapps/javaappbuilt/target/gs-maven-0.1.0-shaded.jar
[INFO] Dependency-reduced POM written at: /home/vagrant/built_projects/builtjavaapps/javaappbuilt/dependency-reduced-pom.xml
[INFO] Dependency-reduced POM written at: /home/vagrant/built_projects/builtjavaapps/javaappbuilt/dependency-reduced-pom.xml
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 2.561 s
[INFO] Finished at: 2018-08-13T04:23:54-04:00
[INFO] ------------------------------------------------------------------------
We are done here
The current local time is: 04:23:55.074
Hello world!
```

## Success verification

Since the script displays built logs to STDIN, it's quite easy to track any build errors.
The expected output from the app itself is:

"The current local time is: 04:23:55.074

Hello world!"

If you see it at the end of script's output, then everything went smoothly.
