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
# Original Repo

https://github.com/rverton/webanalyze

Credit and thanks to rverton!
