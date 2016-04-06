Links
=====
What follows is a collection of links which I have found to be particularly valuable.
The list is somewhat actively maintained. Enjoy!

Tooling/Compilers
-----------------
 - [GDB to LLDB Command Map](http://lldb.llvm.org/lldb-gdb.html)
 - [GCC Extensions to the C Language](https://gcc.gnu.org/onlinedocs/gcc/C-Extensions.html)
 - [Clang Compiler Extensions](http://clang.llvm.org/docs/LanguageExtensions.html)
 - [GCC Extensions to the C Language: Appendix - Linux System Programming](http://archive.oreilly.com/pub/a/linux/excerpts/9780596009588/gcc-extensions-to-the-c-language.html)

Memory Management
-----------------
### Malloc Implementations
 - [nedmalloc](https://github.com/ned14/nedmalloc)
 - [tcmalloc](http://goog-perftools.sourceforge.net/doc/tcmalloc.html)
 - [ptmalloc](http://www.malloc.de/en/)
 - [jemalloc](http://www.canonware.com/jemalloc/)
 - [rtmalloc](http://unix.superglobalmegacorp.com/xnu/newsrc/osfmk/kern/rtmalloc.c.html)
 - [Phkmalloc](https://buildsecurityin.us-cert.gov/articles/knowledge/coding-practices/phkmalloc)

Network Programming
-------------------
### General:
 - [Beej's Guide to Network Programming](http://beej.us/guide/bgnet/output/html/singlepage/bgnet.html)
 - [(comp.unix.programmer) Unix-socket-faq for network programming](http://www.faqs.org/faqs/unix-faq/socket/)

### Advanced Techniques:
 - [The C10K Problem](http://www.kegel.com/c10k.html) - Classic paper on modern concurrency issues and IO strategies
 - [High-Performance Network Programming in C](http://www.linuxjournal.com/article/9815?page=0,1) - Overview of some advanced topics in network programming (gather/scatter IO, mmap'ed files, etc)
 - [Zero-Copy I: User Mode Perspective](http://www.linuxjournal.com/article/6345) - Excellent little breakdown on strategies to reduce copy operations in network IO
 - [Topics in High-Performance Messaging](https://www.informatica.com/downloads/1568_high_perf_messaging_wp/Topics-in-High-Performance-Messaging.htm) - Brief summaries on a number of important TCP/UDP network concepts
 - [High-Performance Network Programming Part 1](http://www.ibm.com/developerworks/aix/library/au-highperform1/) - Basic performance-related network programming techniques
 - [High-Performance Network Programming Part 2](http://www.ibm.com/developerworks/aix/library/au-highperform2/) - More basic performance-related network programming techniques
 - [The SO_REUSEPORT Socket Option](https://lwn.net/Articles/542629/) - How to allow multiple process/threads to listen on a common port without sharing a common socket
 - [Coping with the TCP TIME-WAIT state on busy Linux servers](http://vincent.bernat.im/en/blog/2014-tcp-time-wait-state-linux.html) - Comprehensive overview of TCP TIME_WAIT, how to know if it's an actual problem, and strategies for dealing with it appropriately when it is.

### TCP Flow Control:
 - [TCP_NODELAY and Small Buffer Writes](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_MRG/1.2/html/Realtime_Tuning_Guide/sect-Realtime_Tuning_Guide-Application_Tuning_and_Deployment-TCP_NODELAY_and_Small_Buffer_Writes.html) - Information on using TCP_NODELAY to suppress automatic TCP coalescing (e.g. Nagle's algorithm) by the kernel
 - [TCP_CORK: More than you ever wanted to know](http://baus.net/on-tcp_cork/) - Information on using TCP_CORK to manually coalesce outgoing TCP data

### Security:
 - [Defenses Against TCP SYN FLooding Attacks](http://www.cisco.com/web/about/ac123/ac147/archived_issues/ipj_9-4/syn_flooding_attacks.html)

### Mobile:
 - [Secrets of Mobile Network Performance](http://www.aosabook.org/en/posa/secrets-of-mobile-network-performance.html)
 - [Apple: Designing for Real-World Networks](https://developer.apple.com/library/mac/documentation/NetworkingInternetWeb/Conceptual/NetworkingOverview/WhyNetworkingIsHard/WhyNetworkingIsHard.html)

### Handling SIGPIPE:
 - [Prevent A Process from Terminating When Writing to a Broken Pipe](http://www.microhowto.info/howto/prevent_a_process_from_terminating_when_writing_to_a_broken_pipe.html) - Various strategies for dealing with SIGPIPE
 - [Ignore SIGPIPE without affecting other threads in a process](http://www.microhowto.info/howto/ignore_sigpipe_without_affecting_other_threads_in_a_process.html) - How-to on thread-specific signal blocking

### TCP/IP Tuning
 - [Linux TCP/IP Tuning for Scalability](http://www.lognormal.com/blog/2012/09/27/linux-tcpip-tuning/)
 - [Enabling High Performance Data Transfers](http://www.psc.edu/index.php/networking/641-tcp-tune)
 - [Linux Tuning](http://fasterdata.es.net/host-tuning/linux/)
 - [TCP Tuning Parameters for Different OS's](http://proj.sunet.se/E2E/tcptune.html)
 - [Administer Linux on the Fly](http://www.ibm.com/developerworks/linux/library/l-adfly/index.html)
 - [IPV4 Tuning](http://www.linuxinsight.com/proc_sys_net_ipv4.html)
 - [Let's Make TCP Faster](http://googlecode.blogspot.com/2012/01/lets-make-tcp-faster.html)
 - [Speeding Up Networking - Van Jacobson Presentation](http://www.lemis.com/grog/Documentation/vj/lca06vj.pdf)

### Scalability
 - [Scalability Comparison of Various *nix Systems](http://bulk.fefe.de/scalability/)

I/O
---

### General I/O
 - [libev](http://software.schmorp.de/pkg/libev.html) - High performance event-loop library
 - [libeio](http://software.schmorp.de/pkg/libeio.html) - Libeio is a full-featured asynchronous I/O library for C, modelled in similar style and spirit as libev

### Networking
 - [nanomsg](http://nanomsg.org/) - "a socket library that provides several common communication patterns. It aims to make the networking layer fast, scalable, and easy to use"

Optimization
------------
 - [Optimization of Computer Programs in C](http://leto.net/docs/C-optimization.php)
 - [The Lost Art of C Structure Packing](http://www.catb.org/esr/structure-packing/)
 - [Bit Twiddling Hacks](https://graphics.stanford.edu/~seander/bithacks.html)
 - [Fast to_lower for C](https://github.com/andrew-canaday/fast_tolower/)

Concurrency
-----------
### Patterns
 - [Go Channels in Good old C](http://devcry.heiho.net/2012/07/go-channels-in-good-old-c.html)
 - [The Disruptor Pattern](http://lmax-exchange.github.io/disruptor/files/Disruptor-1.0.pdf)
 - [A Potted Guide to Stackless Coroutines](http://blog.think-async.com/2010/03/potted-guide-to-stackless-coroutines.html)
 - [Boost Proactor](http://www.boost.org/doc/libs/1_47_0/doc/html/boost_asio/overview/core/async.html)
 - [Introduction to Non-blocking IO](http://www.kegel.com/dkftpbench/nonblocking.html)

### Techniques
 - [Coroutines in C](http://www.chiark.greenend.org.uk/~sgtatham/coroutines.html)
 - [Tony Finch - Coroutines in less than 20 lines of standard C](http://fanf.livejournal.com/105413.html)
 - [Coroutines in one page of C](http://www.embeddedrelated.com/showarticle/455.php)
 - [Building Coroutines](http://www.csl.mtu.edu/cs4411.ck/www/NOTES/non-local-goto/coroutine.html)

### Coroutine Libraries for C
 - [libwire](https://github.com/baruch/libwire)
 - [libconcurrency](https://code.google.com/p/libconcurrency/)
 - [C coroutines](https://github.com/stevedekorte/coroutine)
 - [libconcurrent](https://github.com/sharow/libconcurrent)
 - [libcoroutine](https://github.com/sos22/libcoroutine)
 - [libcoro](http://software.schmorp.de/pkg/libcoro.html)
 - [libpcl](http://www.xmailserver.org/libpcl.html)

### Green Threads Libraries for C
 - [State Threads](http://state-threads.sourceforge.net/)

### Fibers Libraries for C
 - [libevfibers](http://olkhovskiy.me/libevfibers/)
 - [libevfibers on github](https://github.com/Lupus/libevfibers)

### Misc
 - [A Gigantic List of Alternate Concurrency Libraries for C](https://github.com/baruch/libwire/wiki/Other-coroutine-libraries)

C/C++
-----
 - [A Guide to Undefined Behavior in C and C++: Part 1](http://blog.regehr.org/archives/213)
 - [A Guide to Undefined Behavior in C and C++: Part 2](http://blog.regehr.org/archives/226)
 - [A Guide to Undefined Behavior in C and C++: Part 3](http://blog.regehr.org/archives/232)
 - [What Every C Programmer Should Know about Undefined Behavior](http://blog.llvm.org/2011/05/what-every-c-programmer-should-know.html)
 - [The C++ Faq](http://www.parashift.com/c++-faq/) - Marshall Cline's invaluable resource for C++ programmers
 - [The C++ Super-Faq](https://isocpp.org/faq) - A wiki combination of Marshall Cline’s C++ FAQs and Bjarne Stroustrup’s C++ FAQ
 - [How to Handle OOM in C](http://eli.thegreenplace.net/2009/10/30/handling-out-of-memory-conditions-in-c)

### OOP-like Modelling in C
 - [SO: How Can Inheritance Be Modelled in C](http://stackoverflow.com/questions/1237266/how-can-inheritance-be-modelled-using-c)
 - [SO: What Techniques/Strategies do People Use for Building Objects in C](http://stackoverflow.com/questions/1225844/what-techniques-strategies-do-people-use-for-building-objects-in-c-not-c)
 - [Object-oriented Programming in C](http://modelingwithdata.org/arch/00000035.htm)
 - [Open Reusable Object Models](http://www.vpri.org/pdf/tr2006003a_objmod.pdf)
 - [Object Oriented Programming in C - Laurent Deniau](http://ldeniau.home.cern.ch/ldeniau/html/oopc/oopc.html)

Assembly Language Programming
-----------------------------
 - [Linux ASM Quickstart](http://database.sarang.net/study/linux/asm/linux-asm.txt)
 - [GCC Inline-assembly HOWTO](http://www.ibiblio.org/gferg/ldp/GCC-Inline-Assembly-HOWTO.html)

Kernel
------
 - [Interfacing with the Scheduler](http://www.gnu.org/software/libc/manual/html_mono/libc.html#Priority)
 - [Linux "Hello World" Kernel Module](http://www.tldp.org/LDP/lkmpg/2.6/html/x121.html)

Misc
----
### Websites/Blogs
 - [The good-looking textured light-sourced bouncy fun smart and stretchy page](http://freespace.virgin.net/hugo.elias/) - Why would you not click this?
 - [libecb](http://software.schmorp.de/pkg/libecb.html) - This project delivers you many gcc builtins, attributes and a number of generally useful low-level functions, such as popcount, expect, prefetch, noinline, assume, unreachable and so on
 - [Eli Bendersky's Website](http://eli.thegreenplace.net/)
 - [Doug Lea's Homepage](http://gee.cs.oswego.edu/)
 - [John Regehr's Blog](http://blog.regehr.org/)
 - [Christian Plesner Hansen](http://h14s.p5r.org/)
 - [The "Double Check Locking is Broken" Declaration](http://www.cs.umd.edu/~pugh/java/memoryModel/DoubleCheckedLocking.html)

### Amazing tricks you will probably never need
 - [Duff's Device](http://www.lysator.liu.se/c/duffs-device.html)
 - [Fast Inverse Square Root](http://h14s.p5r.org/2012/09/0x5f3759df.html)

Standards
---------
### Internet/Networking
 - [IPv4](https://tools.ietf.org/html/rfc791)
 - [IPv6](https://tools.ietf.org/html/rfc2460)
 - [UDP](https://tools.ietf.org/html/rfc768)
 - [TCP](https://tools.ietf.org/html/rfc793)
 - [HTTP/1.0](https://tools.ietf.org/html/rfc1945)
 - [HTTP/1.1 (Original RFC)](https://tools.ietf.org/html/rfc2616)
   - [HTTP/1.1 Message Syntax and Routing](https://tools.ietf.org/html/rfc7230)
   - [HTTP/1.1 Semantics and Content](https://tools.ietf.org/html/rfc7231)
   - [HTTP/1.1 Conditional Requests](https://tools.ietf.org/html/rfc7232)
   - [HTTP/1.1 Range Requests](https://tools.ietf.org/html/rfc7233)
   - [HTTP/1.1 Caching](https://tools.ietf.org/html/rfc7234)
   - [HTTP/1.1 Authentication](https://tools.ietf.org/html/rfc7235)
 - [HTTP/2.0](https://tools.ietf.org/html/rfc7540)
 - [HPACK](https://tools.ietf.org/html/draft-ietf-httpbis-header-compression-12)
 - [QUIC](https://github.com/devsisters/libquic)
 - [RFC6455 (WebSockets)](https://tools.ietf.org/html/rfc6455)
 - Pre-Standard WebSockets Specs:
   - [hybi-10](http://tools.ietf.org/html/draft-ietf-hybi-thewebsocketprotocol-10)
   - [hybi-7](http://tools.ietf.org/html/draft-ietf-hybi-thewebsocketprotocol-07)
   - [hybi-00](http://tools.ietf.org/html/draft-ietf-hybi-thewebsocketprotocol-00)
   - [hixie-76](http://tools.ietf.org/html/draft-hixie-thewebsocketprotocol-76)
   - [hixie-75](http://tools.ietf.org/html/draft-hixie-thewebsocketprotocol-75)
 - [TLS](https://tools.ietf.org/html/rfc2246)
 - [MQTT 3.1.1](http://docs.oasis-open.org/mqtt/mqtt/v3.1.1/os/mqtt-v3.1.1-os.html)

### Compression
 - [zlib](https://tools.ietf.org/html/rfc1950)
 - [deflate](https://tools.ietf.org/html/rfc1951)
 - [gzip](https://tools.ietf.org/html/rfc1952)
 - [sdch](http://lists.w3.org/Archives/Public/ietf-http-wg/2008JulSep/att-0441/Shared_Dictionary_Compression_over_HTTP.pdf)
 - [xz](http://en.wikipedia.org/wiki/Xz)
 - [lzma](http://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

