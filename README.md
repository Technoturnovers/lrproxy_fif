# lrproxy_fif

A compatibility wrapper core for running Code Mystics's *Fix-It Felix Jr.* port for libretro under non-AtGames environments.

## Build

It's just two files, so just build a shared library out of them, using `-DPROXY_FOR=file` to specify the location of 'fif_libretro.so'. Currently, this must be an absolute path or relative path to your working directory.

```
$ gcc -O2 -fPIC -shared -o proxy_core.so lrproxy.c dynlib.c -DPROXY_FOR=./fif_libretro.so
```

By default this logs every libretro API call, use `-DQUIET` to make it less verbose.

## TODO

* Configure core location at runtime, or use RetroArch core directory
* Fix the screwed up aspect ratio somehow
* Use more correct/stylistically sound info fields
* Capture game RNG seeds

PRs welcome.

## License

MIT, original project by leiradel (I only added less than 10 lines).
