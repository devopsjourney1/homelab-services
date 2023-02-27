# Why this is here

Let's Encrypt will dump a file named acme.json in here and it will contain all the certificates it has generated.  This file needs to be mapped to the container so it can be used by Traefik.  Certificates are meant to be secured so make sure you secure this directory.