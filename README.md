Example how to build a GoLang application with Maven and [the mvn-golang-wrapper plugin](https://github.com/raydac/mvn-golang).   
Just clone the project and build with `mvn package`

# What to do if I want to use already installed SDK?
In the case just define `<goRoot>` in plug-in configuration
```
<goRoot>some/folder/where/go</goRoot>
````
and plug-in will be using already installed distributive   
Especially such situation will be for platforms which don't have .zip or .tar.gz distibutive on the GoLang server, because the plug-in knows how to work only with zip and tar packages.

# I want to use values of already defined environment variables!
By defaut the plug-in using only parameters defined in its configuration, if you want to enable import of environment parameters $GOROOT, $GOOS, $GOARCH and $GOROOT_BOOTSTRAP (if they defined), then just add flag `<useEnvVars>`into plug-in configuration
```
<useEnvVars>true</useEnvVars>
```
