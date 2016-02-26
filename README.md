OAuth 1.0 Library for [Go](http://golang.org)
========================

WARNING: This fork is meant to work behind an SSL-terminated load balancer that
subsequently passes the request on as HTTP instead of HTTPS. Both the protocol and 
the method have been selectively statically set. 

THIS FORK WILL NOT WORK IN A TYPICAL HOSTING ENVIRONMENT.
Instead, use the original here: [github.com/mrjones/oauth](github.com/mrjones/oauth)

[![GoDoc](http://godoc.org/github.com/mrjones/oauth?status.png)](http://godoc.org/github.com/mrjones/oauth)

(If you need an OAuth 2.0 library, check out: http://code.google.com/p/goauth2/)

Developing your own apps, with this library
-------------------------------------------

* First, install the library

        go get github.com/mrjones/oauth

* Then, check out the comments in oauth.go

* Or, have a look at the examples:

    * Netflix

            go run examples/netflix/netflix.go --consumerkey [key] --consumersecret [secret] --appname [appname]

    * Twitter
    
        Command line:

            go run examples/twitter/twitter.go --consumerkey [key] --consumersecret [secret]
            
        Or, in the browser (using an HTTP server):
        
            go run examples/twitterserver/twitterserver.go --consumerkey [key] --consumersecret [secret] --port 8888        

    * The Google Latitude example is broken, now that Google uses OAuth 2.0

Contributing to this library
----------------------------

* Please install the pre-commit hook, which will run tests, and go-fmt before committing.

        ln -s $PWD/pre-commit.sh .git/hooks/pre-commit

* Running tests and building is as you'd expect:

        go test *.go
        go build *.go




