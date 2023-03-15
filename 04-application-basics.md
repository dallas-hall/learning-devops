# Application Basics <!-- omit in toc -->

I knew some of this from learning to program in Java and Python but I NodeJS was all new to me.

## Table of Contents <!-- omit in toc -->

- [Overview](#overview)
- [Java](#java)
- [NodeJS](#nodejs)
- [Python](#python)

## Overview

![](images/apps01.png)

![](images/apps02.png)

![](images/apps03.png)

* Interpretted languages are implicity compiled into byte code and then run.
* Without byte code the program can only run on the CPU architecture it was compiled on. So applications had to be compiled on all of the CPU architectures that they would run on.

![](images/apps04.png)

* Modern programming languages compile into byte code which can then be run on any CPU architecture by the interpretter.

![](images/apps05.png)

* Files containing Python byte code have the extensions `.pyc`
* The Python byte code files are run by the Python interpretter inside of a virtual machine. This is not the same as infrastructure VMs.
* The Python VM is responsible for translating the byte code into the required machine code.
* All of this happens in the background when you execute the program.

![](images/apps06.png)

* Code that can be reused by anyone is either known as packages, libraries, or modules.
* If packages are used in a program they must be installed alongside the program as the program is dependent upon them to run. They are known as dependencies.
* Packages are availabe through package managers, such as `pip` for Python.

![](images/apps07.png)

* CI/CD pipelines automate the repeated processes in software development, such as build (i.e compile), test, package, and deploy.

## Java

* Java 9 made a lot of backwards incompatible changes which is why a lot of apps are stuck at Java 1.8.
* The naming scheme for Java dropped the 1 dot after version 9, so instead of Java 1.9 it became Java 9.

![](images/java01.png)

```bash
# Add the Java install path to PATH so the binaries are available
export JAVA_HOME=/path/to/jdk-install
export PATH=$JAVA_HOME/bin:$PATH
```

* Java 9 also introduced the bundling of the JRE inside of the JDK. Java 1.8 and earlier required the JDK and JRE to be installed separately.

![](images/java02.png)

![](images/java03.png)

* Java source code is compiled into Java byte code that can run on any CPU architecture that the Java Virtual Machine (JVM) supports.
* This enables Java apps to built once and run anywhere with a JVM.

![](images/java04.png)

* A Java Archive (JAR) file is used to package Java applications.

![](images/java05.png)

* A Web Archive (WAR) file is used to package Java applications and their web assets (e.g. HTML and CSS files).
* The `META-INF/MANIFEST.MF` is a metadata file. One thing it contains the entry point (`Main-Class:`) for the application.
* The entry point for a Java application is the Java class that contains the `main` method which executes the entire program.

![](images/java06.png)

![](images/java07.png)

* Simple Java apps can easily be built manually.

![](images/java08.png)

* Large Java apps are complicated and should be built using build tools like Ant Maven, or Gradle.
* Build tools contain configuration files where you can specify the steps to build the application in a repeatble manner.

![](images/java09.png)

![](images/java10.png)

![](images/java11.png)


## NodeJS

## Python
