# mod_bw (for Mac OS X 10.10)
Bandwidth Limiter for Apache httpd Server running on Apple Mac OS X 10.10 Yosemite


<strong>How to compile</strong>
-------
Running
```sudo apxs -i -a -c mod_bw.c``` will build the module and install it here: ```/usr/libexec/apache2/mod_bw.so```.

Note: Xcode command line tools have to be installed.

<strong>Install precompiled module</strong>
-------
Alternatively copy the precompiled ```bin/mod_bw.so``` file to ```/usr/libexec/apache2/mod_bw.so```.

The module has been built for Apache/2.4.9 (as shipped with Mac OS X 10.10.2).

<strong>Sample Configuration</strong>
-------
One way of using this module is to limit the bandwidth on a virtual host.

The default configuration file can be found at this location: ```/private/etc/apache2/extra/httpd-vhosts.conf```

You may add the following lines to one of your VirtualHosts like this:

	<VirtualHost 127.0.0.1:80>
	...
	BandwidthModule On
	ForceBandWidthModule On
	# limit total bandwidth to 10MBit/s
	Bandwidth all 10485760
	...
	</VirtualHost>

<strong>Documentation</strong>
-------
For documentation see here:
[http://bwmod.sourceforge.net](http://bwmod.sourceforge.net) or have a look at the ```mod_bw.txt``` file.
