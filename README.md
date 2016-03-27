Example how to build a GoLang application with Maven and [the mvn-golang-wrapper plugin](https://github.com/raydac/mvn-golang).   
Just clone the project and build with `mvn package`

# What to do if I want to use already installed SDK?
In the case just define `<goRoot>` in plug-in configuration
```
<goRoot>some/folder/where/go</goRoot>
````
and plug-in will be using already installed distributive
