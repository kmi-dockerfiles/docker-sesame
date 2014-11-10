(Unofficial) Sesame Docker Image
================================

Docker container for [Sesame RDF Store](http://rdf4j.org)

Usage
-----
To create the image 'openuniversity/sesame', execute the following command on the docker-sesame folder:  

	docker build -t openuniversity/sesame .
	
(Note: do not forget to include the final '.' in the line above)

To run the image and bind to port 8080:

	docker run -d -p 8080:8080 openuniversity/sesame
		
When you launch the container a new user and password will be created for the Tomcat manager (see logs).

Configuration
-------------

By default the memory devoted to Sesame is setup to 256 MB. You may configure this using the `JAVA_MAXMEMORY` environment variable:
	
	docker run -d -p 8080:8080 -e JAVA_MAXMEMORY=512 openuniversity/sesame
	
By default Sesame's data will be stored at /data. You may configure this using the `SESAME_DATA` environment variable:
	
	docker run -d -p 8080:8080 -e SESAME_DATA="/myfolder" openuniversity/sesame

Source
------
The source for this docker contained is [available on GitHub](https://github.com/kmi-dockerfiles/docker-sesame).
See [RDF4J.org](http://rdf4j.org) for Sesame's source code.

Issues
------
Please report any issues on [GitHub](https://github.com/kmi-dockerfiles/docker-sesame/issues).