#salamati

ROGUE Basic Client

##Build Instructions
**Example**

```ant -f suitesdk/build.xml -Dapp.path=../webapp/ -Dsdk.build=../build -Dapp.name=salamati package```

 * suitesdk/build.xml = path/to/OpenGeoClientSDK/ant/script
 * app.path = path/to/webapp/source/code
 * sdk.build = path/to/output/build/directory
 * app.name = name of packaged war file
 * package = ant target to build and package war file

**N.B.** The ant script does not contain a clean step so you may have to add one for local builds.

See [here](http://suite.opengeo.org/opengeo-docs/usermanual/tutorials/clientsdk.html) for more information about the OpenGeo ClientSDK.

##Deploying the war
Here are some ways to deploy the generated war file (there are probably others):
 * Copy the war file to your J2EE container's webapps folder, i.e. .../tomcat7/webapps
 * Use the Tomcat Manager web app, or equivalent for other J2EE container, to deploy an uploaded war
 * Use the *deploy* target in the suitesdk/build.xml ant script to deploy using [Cargo](http://cargo.codehaus.org/)
 * Set up a custom [Cargo](http://cargo.codehaus.org/) deployment