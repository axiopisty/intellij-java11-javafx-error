# intellij-java11-javafx-error

## Abstract

This repository has been created as a SSCCE demonstrating
that IntelliJ is unable to run a maven built JavaFX application
running on OpenJDK 11.

## Actual Error

Open the project with IntelliJ. Open the Main class and try to run the main method from within IntelliJ.
You will see the following error reported:

<pre>Error: JavaFX runtime components are missing, and are required to run this application</pre>

## Expected Results

Intellij should run the application without reporting an error. For example, running the application
directly from the command line works as expected:

<pre>mvn clean install && java -jar target/intellij-java11-javafx-error-0.0.1-SNAPSHOT.jar</pre>

## IntelliJ Environment

<pre>
IntelliJ IDEA 2018.2.5 (Ultimate Edition)
Build #IU-182.4892.20, built on October 16, 2018
JRE: 1.8.0_152-release-1248-b19 amd64
JVM: OpenJDK 64-Bit Server VM by JetBrains s.r.o
</pre>

## System Environment

<pre>
Apache Maven 3.6.0 (97c98ec64a1fdfee7767ce5ffb20918da4f719f3; 2018-10-24T12:41:47-06:00)
Maven home: /home/axiopisty/.sdkman/candidates/maven/current
Java version: 11.0.1, vendor: Oracle Corporation, runtime: /home/axiopisty/.sdkman/candidates/java/11.0.1-open
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "4.4.0-137-generic", arch: "amd64", family: "unix"
</pre>

# Questions for JetBrains

1. Does Intellij include (and run on) a prepackaged JRE rather than running on the version I have installed on my OS? (If so does this mean IntelliJ is running on JRE: 1.8.0_152-release-1248-b19 amd64?


