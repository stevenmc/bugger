bugger
======

Remote console based on NodeJS and Websockets NPM to log errors from remote client and inject code.

This project is an extension of:

https://gist.github.com/2031681

And uses Node NPM Websockets (if using on Windows, you need to install distributable C++)
https://github.com/Worlize/WebSocket-Node

== Use ==

Run the monitor.html in your own webserver, such as http://localhost/monitor.html and add the two JS lines of target.html into any page you're working
on (or simply modify target.html).  Run [monitor-ip]/target.html on the device you want to remotely monitor.  E.g. http://192.168.1.252/target.html

Ensure that any JS you add to target.html is added AFTER the existing code.

Any errors in the target.html file/js will show on your monitor.html page (on the other device you're using).  Equally, on that device, you can now
inject JS, such as:
alert("Hello, world!");

== Known Bugs ==

Websockets is not supported by many browsers including Android 4.

I'll need to upgrade this to use socket.io for wider support.