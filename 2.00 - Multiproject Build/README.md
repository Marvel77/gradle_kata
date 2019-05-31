###Tutorial
[https://guides.gradle.org/creating-multi-project-builds](creating multi-project build)
[https://docs.gradle.org/current/userguide/multi_project_builds.html](authoring multi-project-builds)

[https://docs.gradle.org/current/userguide/intro_multi_project_builds.html](executing multi-rpoject builds)




### Kata
1. Create a root project
1. (Optional) Configure the wrapper to work behind a proxy using project specific properties
    ```
    systemProp.http.proxyHost=...
    systemProp.http.proxyPort=...
    systemProp.https.proxyHost=...
    systemProp.https.proxyPort=...
    systemProp.javax.net.ssl.trustStore=...
    systemProp.javax.net.ssl.trustStorePassword=...
    ```
    
    use
    
    `keytool -import -alias proxy -file proxy.cer -keystore cacert`
    
    command to add a non-trusted proxy certificate to your keystore 
2. Check the version of the gradle wrapper
3. Pin the current wrapper version to `build.gradle`
3. Change the root project's name to `awesome_multi_project`
4. Configure all your subprojects AND your root project, add JCenter repository for all projects
5. Configure your subprojects ONLY, add a version project variable to your subprojects
7. Create a Java Library subproject called `peppered-lib`
8. Include the Java Library subproject to the root project
8. Make sure the Java Library subproject is included - list projects in the build with the wrapper command 
8. Create a class called `GreetingFormatter` inside the Java Library suproject
```
    public class GreetingFormatter {
    
        public static String greeting(final String name) {
            return "Hello, " + name + "!";
        }
    }
```
13. Create a Java Application subproject called `spicy-app`
    * integrate the Spock testing framework to the subproject as a testing tool
14. Include the Java Application subproject to the root project
8. Make sure the Java Library subproject is included - list projects in the build with the wrapper command
7. Create the following Spock Specification as a unit test
```    
    def "application has a greeting"() {
        setup:
        def app = new App()
    
        when:
        def result = app.greeting
    
        then:
        result != null
        result == 'Hello, mate!'
    }
```        
8. Add the Peppered Lib dependency to the Spicy App project
9. Implement the `App.getGreeting` method to run the Spock Specification 
    
    


