# Why we are doing this?
Geo-referencing IPs is, in a nutshell, converting an IP address, perhaps from an incoming web visitor, a log file, a data file, or some other place, into the name of some entity owning that IP address. There are a lot of reasons you may want to geo-reference IP addresses to country, city, etc., such as in simple ad targeting systems, geographic load balancing, web analytics, and many more applications.


# Problem
We have a very large set of IP addresses, lets say 100.000, and we want to have the city where those ip are comming from.
We want the more effective free solution.
The input would be a CSV file with one column listing the IPs.
The output would be a CSV file with two columns listing the IP and the city.

# Boundaries
GeoIP Lite is the best available free and not hosted resource: http://dev.maxmind.com/geoip/legacy/geolite/
GeoIP Lite has 98% accurancy

# Algorithm
## Brutforce Solution

## Higher efficiency solution.
Assuming that the number of cities is much smaller than the number of IPs and knowing that the IP ranges are defining the cities, we can create an optimized algorithm that:
 - Has less total proccess time.
 - Performs less queries to the GeoIP database. This would also allow us use a hosted and maybe 100% accurate GeoIP service with low cost (assuming that the cost is correlated with the number of queries) and to be independent from network latencies in such a scenario.


# Ruby Implementation
Implement a simple script that takes the input file path and the output file path.

# How to contribute
