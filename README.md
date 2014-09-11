keitai-performance-testing
==========================

Performance test scripts for Project Keitai, the RESTful web service extensions for Sakai

## Pre-requisites

* A working Sakai instance. Project Keitai ships in Sakai 10 but backports are available.
* An installation of [Apache jMeter](http://jmeter.apache.org/download_jmeter.cgi).

## Getting started

1. Clone this repository :)
2. In Sakai, as an administrator, create a site that will be used for testing.
3. In Sakai, as an administrator, import the data/users.csv file to create 4000 sample users. There are 4000 users, you can cut down the number of users if you like.
4. In Sakai, go to the site you created, use Site Info > Add participants and copy the list of users in the data/users-for-sites.csv file, to add all of the users to the site. You can cut down this list of users as well.
5. In Sakai, go to the site you created, add the tools you want to test and as much sample data as required.
6. Configure keitai.properties for your environment.
7. Start JMeter via `./jmeter.sh -p /path/to/keitai.properties`
8. Add the relevant tests to JMeter.
9. Run, analyse data.

## Enhanced testing
The majority of the entity providers provide a 'my' service which gives a view for the user across all sites. For example the gradebook /direct/gradebook/my.json will give you the gradebook items for the current user in all sites.
The performance tests already make a request to the 'my' service so simply adding more sites with the same users will allow you to ramp up the amount of load and get more realistic results.

