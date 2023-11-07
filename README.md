# Introduction

I modified the webanalyze tool for my personal use to output as one single line for the result, making the data easier to view.

Example:
```
https://www.google.com : [Google Web Server,  (Web servers) | HTTP/3,  (Miscellaneous)]
```

# Installation

```
git clone https://github.com/byt3hx/webanalyzer.git
cd webanalyzer/cmd/webanalyzer/
go build main.go
mv main /usr/bin/webanalyzer
```

# Usage

```
Usage of webanalyzer:
  -apps string
        technologies definition file (default "technologies.json")
  -c int
        links to follow from the root page (default 0)
  -l string
        filename with hosts, one host per line.
  -output string
        output format (stdout|csv|json) (default "stdout")
  -r    follow http redirects (default false)
  -s    avoid printing header (default false)
  -search
        searches all urls with same base domain (i.e. example.com and sub.example.com) (default true)
  -u string
        single host to test
  -update
        update technologies file to current dir
  -w int
        number of worker (default 4)
```

```
$ webanalyzer -u https://www.google.com -c 1
 :: webanalyze        : v0.3.7
 :: workers           : 4
 :: technologies      : technologies.json
 :: crawl count       : 1
 :: search subdomains : true
 :: follow redirects  : false

https://www.google.com/imghp?hl=th&tab=wi : [HTTP/3,  (Miscellaneous) | Google Web Server,  (Web servers)]
https://www.google.com : [HTTP/3,  (Miscellaneous) | Google Web Server,  (Web servers)]
```
# Original Repo

https://github.com/rverton/webanalyze

Credit and thanks to rverton!
