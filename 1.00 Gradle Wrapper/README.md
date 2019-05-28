###Tutorial
[https://docs.gradle.org/current/userguide/gradle_wrapper.html](https://docs.gradle.org/current/userguide/gradle_wrapper.html)


### Kata
0. Display help information about the `wrapper` task
1. Generate a specific version (5.2.1) of the Gradle wrapper
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
2. List the wrapper tasks
3. Generate a new Gradle build using the wrapper
3. Execute a build with the wrapper
4. Upgrade the wrapper version (to 5.4.1) using the command line 
5. Pin the wrapper version by configuring the `wrapper` task  
            
            // optional, for version pinning
            wrapper {
                gradleVersion = '5.3.1'
            }
6. Regenerate the wrapper to update the specified version
        
    





