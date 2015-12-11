# EasyMocker
http://sourceforge.net/p/easymocker/home/Home/

# Web Service Mocker

Web Service Mocker is an easy to use, completely web based SOAP web service simulator. This utility is found very useful in a SOA development environment during unit test, preliminary acceptance test, component integration test, regression test and non functional requirement test phases of any project.
Reasons for use

In a test environment, mocked services can simulate the behavior of complex, real (non-mock) service and are therefore useful when a real service is impractical or impossible to incorporate into a test.
Why not soapUI?

* soapUI is a powerful testing tool which also provides mocking facility. The following are the few reasons why this utility is useful over soapUI for web service mocking.
* soapUI is not web based - With this utility a tester/developer can mock a service, change a mocked service easily using any web browser.
* soapUI is not centralized - With this utility all mocked services will be visible for everyone connected over network. No installation required on each machine.
* soapUI is for technical people - To mock a web service in soapUI, which can generate a selective response for a particular request requires knowledge of XPATH, to generate delayed mocking requires knowledge of groovy scripting.
* soapUI is WSDL dependent - Everything in soapUI starts with a WSDL, if you want to mock a service without WSDL it is not possible in soapUI.

# Software Requirement
Apache Tomcat 6 or above - http://tomcat.apache.org
Java Runtime Environment 1.6 or above - http://www.oracle.com/technetwork/java/javase/downloads/index.html

# Installation
Place the war file under (tomcat-root)/webapps directory and start the tomcat server.

# Usage
* Once the tomcat server is started the web page will be available at http://host:port/context/index.jsp
* Ex: If the war name is webservicemocker-0.0.1.war and port is 8080 the web URL will be http://localhost:8080/webservicemocker-0.0.1/index.jsp

# Technical details
Web Service Mocker is a simple web application.
* Core engine is a simple Servlet. This Servlet dispatches the desired response based on end point URL and request parameter
* Front end is a set of JSPs
* soapUI API (3.5) is used to import WSDLs, validate schema and generate skeleton SOAP messages
* SAAJ API is used for generic web service test client
* Log4j API for logging
