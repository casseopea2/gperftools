# Google Performance Tools #

The fastest malloc we've seen; works particularly well with threads and STL. Also: thread-friendly heap-checker, heap-profiler, and cpu-profiler.

## Overview ##

Perftools is a collection of a high-performance multi-threaded malloc() implementation, plus some pretty nifty performance analysis tools.

Perftools is distributed under the terms of the BSD License.

For downloads, news, and other information, visit our [Project Page](http://code.google.com/p/google-perftools).

## Example ##

_Note: this is by no means complete documentation, but simply gives you an idea of what the API is like._

No recompilation is necessary to use these tools.

TC Malloc:
```
gcc [...] -ltcmalloc
```

Heap Checker:
```
gcc [...] -o myprogram -ltcmalloc
HEAPCHECK=normal ./myprogram
```

Heap Profiler:
```
gcc [...] -o myprogram -ltcmalloc
HEAPPROFILE=/tmp/netheap ./myprogram
```

Cpu Profiler:
```
gcc [...] -o myprogram -lprofiler
CPUPROFILE=/tmp/profile ./myprogram
```

## Sample Output ##

The heap profiler can pop up a window that displays information as a directed graph:

![http://google-perftools.googlecode.com/svn/trunk/doc/heap-example1.png](http://google-perftools.googlecode.com/svn/trunk/doc/heap-example1.png)

The cpu profiler can produce a weighted call graph:

![http://google-perftools.googlecode.com/svn/trunk/doc/pprof-vsnprintf.gif](http://google-perftools.googlecode.com/svn/trunk/doc/pprof-vsnprintf.gif)


## Documentation ##

  * [thread-caching malloc](http://google-perftools.googlecode.com/svn/trunk/doc/tcmalloc.html)
  * [heap-checking using tcmalloc](http://google-perftools.googlecode.com/svn/trunk/doc/heap_checker.html)
  * [heap-profiling using tcmalloc](http://google-perftools.googlecode.com/svn/trunk/doc/heapprofile.html)
  * [CPU profiler](http://google-perftools.googlecode.com/svn/trunk/doc/cpuprofile.html)

## Downloads ##

For downloads, please visit our
[Downloads Page](http://code.google.com/p/google-perftools/downloads/list).

## Links to Other Sites ##
Russ Cox's [gperftools-httpd](http://code.google.com/p/gperftools-httpd), a simple http server based on thttpd that enables remote profiling via google-perftool's pprof.

Brett Viren's [Perftools](http://minos.phy.bnl.gov/~bviren/minos/software/prof/PerfTools/) project at the Brookhaven National Laboratory -- a similar project with the same name as Google's. [[docs](http://minos.phy.bnl.gov/~bviren/minos/software/prof/PerfTools/doc/)], [[download](http://minos.phy.bnl.gov/~bviren/minos/software/prof/PerfTools.tgz)]

## Questions and Feedback ##

While this wiki page allows comments, I don't check it very often.  If you have questions, comments, or feedback, please direct them to google-perftools@googlegroups.com.