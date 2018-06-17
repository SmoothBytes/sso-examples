Single Sign-On for PHP (Ajax compatible) Examples
---

There is two example brokers. One with normal redirects and one using
[JSONP](https://en.wikipedia.org/wiki/JSONP) / AJAX.

To proof it's working you should setup the server and two or more brokers, each on their own machine and their own
(sub)domain. However you can also run both server and brokers on your own machine, simply to test it out.

On *nix (Linux / Unix / OSX) run:

    $ export SSO_SERVER=https://yourclub.socialandloyal.com
    $ export SSO_BROKER_ID={id in your club config}
    $ export SSO_BROKER_SECRET={secret in your club config}
    
    $ php -S localhost:9001 -t examples/broker/
    $ php -S localhost:9002 -t examples/ajax-broker/

Now open some tabs and visit http://localhost:9001, http://localhost:9002.

_Note that after logging in, you need to refresh on the other brokers to see the effect._

##Notes

- This is only for login and logout to be able to register new clients you need to use SAL api
- To make it work also it is needed that server and broker use the same protocol https or http

