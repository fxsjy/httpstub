httpstub
========
A simple high performance http server 

* can only serv one file
* can simulate response delay
* based on epoll


`usage:  httpstub -p <port> -f <data file> -d <delay (ms)> [-q quiet]`


Performance
===========
* `httpstub -f README.md -q`

	with "-q", no debug messages written to "stub.log"

* `ab -n10000 -c1000 http://localhost:8402/ `        : 15000 r/s
* `ab -n10000 -c1000 -k  http://localhost:8402/`      : 52000 r/s

* Test Env:

  		$grep MemTotal /proc/meminfo
		MemTotal:      8174464 kB

		$grep 'model name' /proc/cpuinfo
		model name      :        Intel(R) Xeon(R) CPU E7- 2870  @ 2.40GHz
		model name      :        Intel(R) Xeon(R) CPU E7- 2870  @ 2.40GHz
		model name      :        Intel(R) Xeon(R) CPU E7- 2870  @ 2.40GHz
		model name      :        Intel(R) Xeon(R) CPU E7- 2870  @ 2.40GHz

		$uname -a
		Linux ts-rh64-6 2.6.18-308.el5 #1 SMP Fri Jan 27 17:17:51 EST 2012 x86_64 x86_64 x86_64 GNU/Linux
