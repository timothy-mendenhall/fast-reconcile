An OpenRefine reconciliation service for [FAST](http://www.oclc.org/research/activities/fast.html?urlm=159754).

>FAST is available as Linked Data, which is an approach to publishing data which enhances the utility of information on the web by making references to persons, places, things, etc. more consistent and linkable across domains.

The service queries the [FAST AutoSuggest API](http://www.oclc.org/developer/documentation/fast-linked-data-api/request-types)
and provides normalized scores across queries for reconciling in Refine.

Run locally as:
~~~~
$ python reconcile.py --debug
~~~~

Michael Stephens wrote a [demo reconcilliation service](https://github.com/mikejs/reconcile-demo), which Christina Harlow then updated. 

##Changes for this Fork

This version has been tested on OpenRefine 2.8 and Python 3.7 on a Windows 10 computer.  Minor tweaks to C. Harlow's fork of M. Stephens's code have been made to udpate the core reconcile.py for use in Python 3.7 (because of errors generated, at least when used in Windows 10), and additional minor edits have been made to the text.py code to improve recall from the OCLC FAST API--not only do spaces need to be recoded as %20 rather than +, but so do parentheses, colons, commas, and periods, which can especially affect headings in the Title and Event facets, and therefore also the FAST All query type. 

