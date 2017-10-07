# Footprinting CloudFlare domains #

## Methods ##

1. Find other TLDs (takealot.com vs takealot.co.za)
2. Find subdomains
    * ipv4info
		* images.takealot.com	196.34.14.129
		* smtp.takealot.com		196.34.14.130
		* msecure.takealot.com	196.35.76.217
	* Subdomain brute
3. Find typo domains
	* takealote.com		196.14.118.195
	* takeallot.com		196.14.118.195
	* takelot.com		196.14.118.195
4. Historical DNS records
	* static.takealot.com -> 196.34.14.129 -> 104.20.79.212
5. Check surrounding IPs
	* 196.34.14.129 + 1 / 196.34.14.129 - 1
		* takealothealth.com	196.34.14.128
		* take2.co.za			196.34.14.132 -> 196.14.118.195
6. Check Crimeflare database
	* SELECT * FROM country WHERE domain LIKE '%takealot%';
		* takealot.com	196.14.118.195/32	SOUTH-AFRICA
		* takealot.com	196.14.118.196/32	SOUTH-AFRICA
		* takealot.com	196.34.14.131/32	SOUTH-AFRICA
7. Use Censys or Scans.io to get cert info for the domain

## Other ##
1. 1m top domains from Statvoo