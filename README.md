# Spring CVE
This includes CVE-2022-22963, a Spring SpEL / Expression Resource Access Vulnerability, as well as CVE-2022-22965, the spring-webmvc/spring-webflux RCE termed "SpringShell".
     
     
## CVE-2022-22963
In Spring Cloud Function versions 3.1.6, 3.2.2 and older unsupported versions, when using routing functionality it is possible for a user to provide a specially crafted SpEL as a routing-expression that may result in remote code execution and access to local resources.

```
python3 poc-CVE-2022-22963.py targets.txt
```
By default whoami is executed on the target and a file vulnerable.txt is created with the URLs that are vulnerable.


## CVE-2022-22965
A Spring MVC or Spring WebFlux application running on JDK 9+ may be vulnerable to remote code execution (RCE) via data binding. The specific exploit requires the application to run on Tomcat as a WAR deployment. If the application is deployed as a Spring Boot executable jar, i.e. the default, it is not vulnerable to the exploit. However, the nature of the vulnerability is more general, and there may be other ways to exploit it.

```
 python3 poc-CVE-2022-22965.py  --file target.txt
 ```

## references
* [CVE-2022-22963](https://tanzu.vmware.com/security/cve-2022-22963)
* [CVE-2022-22965](https://tanzu.vmware.com/security/cve-2022-22965)
