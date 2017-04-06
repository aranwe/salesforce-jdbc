# sforce-jdbc
Salesforce JDBC driver allows Java programs to connect to a Salesforce data services using standard, database independent Java code. Is an open source JDBC driver written in Pure Java, and communicates over SOAP/HTTP(S) protocol.
The main purpose of the driver is to retrieve (only) data from Salesforce services for data analysis. Primary target platform for the driver usage is Eclipse BIRT engine.

## Supported Salesforce and Java versions
The current version of the driver should be compatible with **Salesforce Partner API version 39.0 and higher** and **Java 8**.

## Get the driver
Download the driver [here](https://www.driver.com)

## How to connect
Driver class name: com.ascendix.jdbc.salesforce.ForceDriver 
Database URL: jdbc:ascendix:salesforce://
Sample connection string: jdbc:ascendix:salesforce://;User=myname@companyorg.com.xre.ci;Password=passwordandsecretkey

**Warning!** password provided has to contain your password and secret key in one sting;

## Supported features
1. Queries supports native SOQL.
2. Request caching support on local drive. Canching supports 2 modes: global and session. Global mode means that the cached result will be accessible for all system users for certain JVM session. Session cache mode works for each Salesforce connection session separately. Both modes cache stores request result while JVM still running but no longer than for 1 hour. How to use cache feature:
  * Global cache mode:
  ```SQL
  GLOBAL CACHE SELECT Id, Name FROM Account
  ```
  * Session cache mode
  ```SQL
  SESSION CACHE SELECT Id, Name FROM Account
  ```

## Limitations
1. Nested queries support is under development.

### Sponsors
[Ascendix Technologies Inc.](https://ascendix.com/) <img src="http://ww1.prweb.com/prfiles/2006/12/12/490667/ascendixlogo.jpg" width=100 align="right"/>
