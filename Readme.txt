Create a new Spring Boot application. Name the project "springCloudConfigServerDemo”, and use this value for the Artifact. Use Jar packaging and the latest versions of Java. Spring boot version will be taken automatically. Use "config server" while creating the project.

Edit the main Application class (probably named springCloudConfigServerDemo). Add the @EnableConfigServer to this class.

Create a new repository on GitHub to hold your application configuration data. Call the repository "ConfigData" or a name of your choosing. Note the full URI of the repository, you will need this in a following step.

Add a new file to your GitHub repository called  "configuration.properties". Add a key called "appname" and a value of "SpringCloudConfigServerDemo". (add anothey key value if needed)

Back in your project, create an  application.properties file in the root of your classpath (src/main/resources recommended). Add the key "spring.cloud.config.server.git.uri" and the value "https://github.com/"YOUR-GITHUB-ID"/ConfigData", substituting the value for Github ID and repository name as needed. Also set the “server.port” to 8001.

Run the application. Open the URL http://localhost:8001/configuration/default. You should see the JSON result that will actually be used by Spring. If the server is not working, review the prior steps to find the issue before moving on.