# A simple, minimal Maven example: hello world

Taken from https://github.com/pdurbin/maven-hello-world

To create the files in this git repo we've already run `mvn archetype:generate` from http://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

    mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

Now, to print "Hello World!", type either...

    cd my-app
    mvn compile
    java -cp target/classes com.mycompany.app.App

or...

    cd my-app
    mvn package
    java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App

Running `mvn clean compile exec:java` requires http://mojo.codehaus.org/exec-maven-plugin/

Running `java -jar target/my-app-1.0-SNAPSHOT.jar` requires http://maven.apache.org/plugins/maven-shade-plugin/
