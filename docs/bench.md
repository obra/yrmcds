#<cldoc:Benchmark Results>

Benchmark results.

Environment
-----------

* CPU  
    Intel Xeon E5507 2.27 GHz * 2 (total 8 physical cores)
* OS  
    Ubuntu 12.04
* Threads  
    8 worker threads for yrmcds / memcached
* Memory  
    1 GiB for yrmcds / memcached
* Buckets  
    5 million for yrmcds

Benchmark Tool
--------------

[memslap][] from [libmemcached][].

Parameters: `--threads=8 --concurrency=80`

Other parameters are left default, i.e., memslap runs for 600 seconds with set/get ratio = 1:9.

memslap ran on a different machine.

Versions
--------

* memcached 1.4.13
* yrmcds 0.9.0

Results
-------

* memcached  
    Ops: 71584331 TPS: 119298 Net_rate: 126.6M/s
* yrmcds (0 slave)  
    Ops: 67408111 TPS: 112337 Net_rate: 110.7M/s
* yrmcds (1 slave)  
    Ops: 60793090 TPS: 101313 Net_rate: 96.2M/s
* yrmcds (2 slaves)  
    Ops: 50795409 TPS: 84651 Net_rate: 81.3M/s


[memslap]: http://docs.libmemcached.org/bin/memaslap.html
[libmemcached]: http://libmemcached.org/libMemcached.html
