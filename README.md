Example how to build a GoLang application with Maven and [the mvn-golang-wrapper plugin](https://github.com/raydac/mvn-golang).   
Just clone the project and build with `mvn package`

# What is Maven?
Maven is very popular tool in Java world allows to build projects and the main power of maven in its central repository which allows to load dependencies without tricks.   
If you have not maven installed on your computer, you can visit its home page and [read instructions how to install](https://maven.apache.org). Also the project contains `mvnw` wrapper which can download maven automatically.

# Build and start
To get compiled example Golang application you should make listed steps:
- (optional step) [download and install JDK](https://bell-sw.com/pages/downloads/#/java-11-lts)
- just clone the repository with `git clone https://github.com/raydac/mvn-golang-example.git`
- go to the cloned project folder
- build the project with `mvn` command if you have installed [maven](https://maven.apache.org/index.html) or with maven wrapper `mvnw` which will download maven automatically
- go to the generated `bin` folder and execute result file named `binResult`

# Screencast
![Screencast](assets/go-mvn-example-screencast.gif)

# Create from archetype
It is possible to create "Hello World" project just from maven archetype
```
mvn archetype:generate -B -DarchetypeGroupId=com.igormaznitsa -DarchetypeArtifactId=mvn-golang-hello -DarchetypeVersion=2.3.8 -DgroupId=com.go.test -DartifactId=gohello -Dversion=1.0-SNAPSHOT
```
if you want to develop multi-module project sharing some sources, you can use muti-module archetype
```
mvn archetype:generate -B -DarchetypeGroupId=com.igormaznitsa -DarchetypeArtifactId=mvn-golang-hello-multi -DarchetypeVersion=2.3.8 -DgroupId=com.go.test -DartifactId=gohello-multi -Dversion=1.0-SNAPSHOT
```


# What to do if I want to use pre-installed Golang SDK?
In the case just define `<goRoot>` in plug-in configuration
```
<goRoot>some/folder/where/go</goRoot>
````
and plug-in will be using already installed distributive   

# I want to export already presented environment variables $GOROOT and $GOPATH
By defaut the plug-in using only parameters defined in its configuration, if you want to enable import of environment parameters $GOROOT, $GOOS, $GOARCH and $GOROOT_BOOTSTRAP (if they defined), then just add flag `<useEnvVars>`into plug-in configuration
```
<useEnvVars>true</useEnvVars>
```
