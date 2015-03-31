# mod_bw
Bandwidth Limiter for Apache httpd Server running on Apple Mac OS X 10.10 Yosemite


<strong>How to compile</strong><br/>
Running
```sudo apxs -i -a -c mod_bw.c```<br/>
will build the module and install it here:
```/usr/libexec/apache2/mod_bw.so```
<br/>Note: Xcode command line tools hav to be installed.

<strong>Install precompiled module</strong><br/>
Alternatively copy the precompiled ```bin/mod_bw.so``` file to
```/usr/libexec/apache2/mod_bw.so```.</br>
The module has been built for Apache/2.4.9 (as shipped with Mac OS X 10.10.2).

<strong>Sample Configuration</strong><br/>
One way of using this module is to limit the bandwidth on a virtual host.

The default configuration file can be found at this location:<br/>```/private/etc/apache2/extra/httpd-vhosts.conf```

You may add the following lines to one of your VirtualHosts like this:<br/>
```<VirtualHost 127.0.0.1:80>```<br/>
```...```<br/>
```BandwidthModule On```<br/>
```ForceBandWidthModule On```<br/>
```# limit total bandwidth to 10MBit/s```<br/>
```Bandwidth all 10485760```<br/>
```...```<br/>
```</VirtualHost>```

<strong>Documentation</strong><br/>
For documentation see here: http://bwmod.sourceforge.net <br/>
or have a look at the ```mod_bw.txt``` file.

