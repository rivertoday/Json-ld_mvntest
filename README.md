# Json-ld_mvntest
This is a demo maven project invoking jsonld-java in git(https://github.com/jsonld-java/jsonld-java)

## How to use it

First, this project is running with eclipse, so I assume you have already made eclipse ready.

Then, I recommend you to configure your own apache-maven inside eclipse, http://maven.apache.org/

It should be very easy.



Okay, now we create a maven project within eclipse.

Edit the pom.xml, adding the following contents:

```
    <dependency>

        <groupId>com.github.jsonld-java</groupId>

        <artifactId>jsonld-java</artifactId>

        <version>0.12.3</version>

    </dependency>
```

And, as indicated in json-ld-java git readme, you put the corresponding example code.

Remember to modify the json file to the one you exported with your protege.

Now, right click your project, choose Debug As/Run As,  "maven build..."

Type the following contents inside the goals textbox:

```
clean dependency:copy-dependencies package
```

After Build Success prompted, you can go to the target folder, and run it as below:

```
java -cp MyFirstMVN-0.0.1-SNAPSHOT.jar;"./dependency/*" com.silverriver.tools.MyFirstMVN.App
```

Good luck!