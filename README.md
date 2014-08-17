keitai-performance-testing
==========================

Performance test scripts for Project Keitai, the RESTful web service extensions for Sakai

## Pre-requisites

* A working Sakai instance. Project Keitai ships in Sakai 10 but backports are available.
* An installation of [Apache jMeter](http://jmeter.apache.org/download_jmeter.cgi).

## Getting started

1. Clone this repository :)
2. Create 5 sites in your Sakai instance: jMeter1, jMeter2, jMeter3, jMeter4, jMeter5. (TODO automate this)
3. Import the set of users for each site. (TODO automate this)
4. Add the tests to jMeter.
5. Run, analyse data.
