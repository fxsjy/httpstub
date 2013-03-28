httpstub
========
A simple high performance http server 

* can only serv one file
* can simulate response delay
* based on epoll


usage:  httpstub -p <port> -f <data file> -d <delay (ms)> [-q quiet]


Performance
===========
* httpstub -f hello.txt -q
* ab -n10000 -c1000 : 8000 r/s
* ab -n10000 -c1000 -k: 25000 r/s
