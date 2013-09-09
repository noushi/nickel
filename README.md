NICKEL
======

This is to test the behavior of Google Chrome browser with jemalloc.


To install requisites on Ubuntu , run: ```make nickel```

To try it out, run: ```./nickel```


NOTES
-----

- Tested on ubuntu 12.04 LTS 64bit

- Forcing Chrome to use jemalloc instead of the multi-allocator mode provides a more reliable experience: 
  * I've had Chrome crash twice using the multi-allocators while running for more than a week and with over 80 tabs
  * with jemalloc, it simply doesn't crash, and the system behaves better when filling all RAM (and having few megs for buffers and cache)
