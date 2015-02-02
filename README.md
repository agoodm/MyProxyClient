MyProxy Client Package
======================
This a pure* Python implementation of a client to the MyProxy Credential
Management Server (http://grid.ncsa.uiuc.edu/myproxy/)

* i.e. MyProxy C client libraries are not required for this package. 

It uses pyOpenSSL to make an SSL connection to the server following the
messaging interface as outlined in: http://grid.ncsa.uiuc.edu/myproxy/protocol/

The code is based on an original program myproxy_logon by Tom Uram of ANL.

Releases
========
1.4.0
-----
 * Fix for SSL to use TLS instead of SSLv3 to address POODLE vulnerability
 * Fix for SSL verification for PyOpenSSL version 0.14 - v1.3.1 was broken
   because it passed the call back method to OpenSSL using verification classes'
   `__call__` method.
   
Tested on CentOS 6.4.
   
1.3.1
-----
 * Fix to MyProxyClient.writeProxyFile and MyProxyClient.readProxyFile to correctly 
   pick-up overridden file setting.  Thanks to Nicolas Carenton, IPSL.

Tests
=====
Unit test module with test files is in test/.  See the README in that directory.

Documentation
=============
Epydoc generated documentation is available in documentation/.  run the 
Makefile to regenerate if required.

Thanks
======
 * to OMII-UK for funding development of NDG Security (2007-2008)
 * Tom Uram who wrote the `myproxy_logon` program on which this package is based.
