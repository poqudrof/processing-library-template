This is another library compilation / distribution template. It works in command line, all is require is bash and maven (and a JDK obviously), so it works directly on OSX and Linux. You can get command line tools for Linux with the [Cygwin](https://www.cygwin.com/) project. 

You can also import in Netbeans, and possible Eclipse, or any other IDE that can read Maven projects. 

### Get the sources 

You can either clone the reposity or download the latest archive in the [Release](https://github.com/poqudrof/processing-library-template/releases) section.

The example comes with an example source file, so it should work out of the box.
To compile you need : Maven, a [JDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (Java Development Kit) that's it ! 


### Compile

Go to the library folder (cloned or unzipped). 
To compile, use the *compile.sh* script, or just type
``` bash
mvn install
mvn javadoc:javadoc 
```

You must edit your library information in the **pom.xml** and **createLibrary.sh** files.

At least you must set the name of the library, and you should also set groupID and artifactID in the pom following the [Maven rules](https://maven.apache.org/guides/mini/guide-naming-conventions.html). 


The library is for Processing 3.0b4, and it will follow the latest version of Processing. 
To create libraries for Processing 2.2.1 (stable) go in **pom.xml** and replace

``` xml
<dependency>
  <groupId>org.processing</groupId>
  <artifactId>core</artifactId>
  <version>3.0b4</version>
</dependency>
```

by

``` xml 
<dependency>
  <groupId>org.processing</groupId>
  <artifactId>core</artifactId>
  <version>2.2.1</version>
</dependency>
```
		
### Deploy 

Use the deployment script :

``` bash
sh createLibrary.sh 
```

You will obtain a file name **LibraryName.tgz** that can be shared to the community.


