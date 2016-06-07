Apache-Shiro-CRSFGuard
============================

This is a version of Apache Shiro web application using OWASP CRSFGuard to protect forms and Post request with a unique token

##About the project
This project can be run from Eclipse Mars using Jetty 
Eclipse Java EE IDE for Web Developers.
Version: Mars Release (4.5.0)
Build id: 20150621-1200

##Instructions
The web app is using Stormpath as OAUTH. In order to run this properly you must obtain a apiKey as instructed in teh Apache Shiro Documentation to setup Strompath:
http://shiro.apache.org/webapp-tutorial.html#step2

##Set a token
To add a protection token to a [post] form you need to add the following hidden field

 ```
 <form name="test1" action="protect.html">
     <input type="text" name="text" value="text"/>
     <input type="submit" name="submit" value="submit"/>
     <input type="hidden" name="<csrf:tokenname/>" value="<csrf:tokenvalue uri="protect.html"/>"/>
 </form>
  ```

