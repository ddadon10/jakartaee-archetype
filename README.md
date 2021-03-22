# Jakarta EE archetype

This is a Jakarta EE archetype with Payara Micro and Google Cloud libraries that I am using to create projects faster

It contains, among others:
* The Payara Micro BOM and Google Cloud Libraries BOM to keep dependencies under control
* Some maven plugins to build and run the application server locally
* A helper resources with a `.reload` file to enable hot reloading on Payara Micro
* A Web Application Deployment Descriptor `web.xml`
* A ready to use `.gitignore` 

It will evolve with the needs I encounter while using it.

## Prerequisite
* JDK 1.8
* Maven 3.6.3

## Installation
Clone this repo and run:
```
mvn install
```

## Use the archetype
On the location where you want the directory to be created:
* Replace the `groupId` and `artifactId` with the values you want
* Run the following maven command:

```
mvn archetype:generate \
-DarchetypeGroupId=sh.david \
-DarchetypeArtifactId=jakartaee-archetype \
-DarchetypeVersion=1.0-SNAPSHOT \
-DarchetypeCatalog=local \
-DinteractiveMode=false \
-DgroupId={AddYourGroupId} \
-DartifactId={AddYourArtifactId}
```

## Start the project created
Go into your project directory and run:
```
mvn install && mvn payara-micro:start
```

## License
Copyright 2021 David Dadon
Licensed under the [Apache License, Version 2.0](https://github.com/ddadon10/jakartaee-archetype/blob/trunk/LICENSE.txt)
