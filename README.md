# Spring CVE
This includes CVE-2022-22963, a Spring SpEL / Expression Resource Access Vulnerability, as well as CVE-2022-22965, the spring-webmvc/spring-webflux RCE termed "SpringShell".
     
     
## CVE-2022-22963
In Spring Cloud Function versions 3.1.6, 3.2.2 and older unsupported versions, when using routing functionality it is possible for a user to provide a specially crafted SpEL as a routing-expression that may result in remote code execution and access to local resources.

```
python3 poc-CVE-2022-22963.py targets.txt
```
By default whoami is executed on the target and a file vulnerable.txt is created with the URLs that are vulnerable.


## CVE-2022-22965


```
 python3 poc-CVE-2022-22965.py  --file target.txt
 ```
