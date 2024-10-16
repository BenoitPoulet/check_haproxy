check_haproxy
-------------

Checks haproxy stats and reports errors if any of the servers for a proxy are down.
 ```
    Usage: check_haproxy.rb [options]

Specific options:
    -u, --url URL                    Statistics URL to check (eg. http://demo.1wt.eu/)
    -p, --proxies [PROXIES]          Only check these proxies (eg. proxy1,proxy2,proxylive)
    -U, --user [USER]                Basic auth user to login as
    -P, --password [PASSWORD]        Basic auth password
    -w, --warning [WARNING]          Pct of active sessions (eg 85, 90)
    -c, --critical [CRITICAL]        Pct of active sessions (eg 90, 95)
    -s, --ssl                        Enable TLS/SSL
    -k, --insecure                   Allow insecure TLS/SSL connections
        --http-error-critical        Throw critical when connection to HAProxy is refused or returns error code
    -m, --metrics                    Enable metrics
    -T, --open-timeout [SECONDS]     Open timeout
    -t, --read-timeout [SECONDS]     Read timeout
    -h, --help                       Display this screen
 ```
Example: ```check_haproxy.rb -u "http://demo.1wt.eu/" -w 80 -c 95```

License
-------

GPL https://www.gnu.org/licenses/gpl.html
