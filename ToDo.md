#ToDo list for the ePing.py project

# Introduction #

ToDo list for the ePing.py project. Also it should show some kind of progress by crossing add/fixed features


# Details #
  * Create a logo
  * Send a log summary once a day by e-mail
  * Create nice graphs or something to show status history
  * Make the content of the e-mail customisable in the configfile.
  * ~~Fix the extended timeout option that I broke~~ edit: extended timeout now works again, and without even changing the timeout value that Python's urllib uses.
  * ~~Instead of only mentioning a short timeout occuring, show how many seconds it eventually took~~
  * ~~Make the urlchecking classes threaded. Right now all the urls are checked after each other. In the event that 15 sites reach a long timeout with timeout values of 5+30 seconds, the check itself will require at least 15`*`(5+30)= 8,75 minutes. This is not really practical (because sometimes I actually get into this situation). By making the UrlChecker class threaded, the total amount of time it takes is decided by the timeout values alone, and not influenced by the amount of urls.~~ edit: done
  * ~~Add ping support :-)~~ edit: seems actually a little bit pointless
  * ~~Perhaps a more advanced log system, based on XML or SQLite~~ edit: just found Python Logging module, should be sufficient for now.
  * Perhaps have it running as a service/daemon
  * ~~Have an easy configuration option/file so no reading through code is required~~ edit: added
  * ~~Put the timeout-values (default and long) in configfile too~~ edit: done, both are now set in the config file.
  * ~~When only default timeout is hit, put it in logfile. Email notification only if high timeout is also reached.~~ edit: done. When an short timeout is reached, only an entry will be made to the log. When a longer timeout is reached, or a different kind of error is found, then an e-mail notification is also send (log still gets entry).