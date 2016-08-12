# Collection of dockerfiles

## Avocado
**avocado-debian**: avocado/debian-avocado/Dockerfile
Basic debian image with avocado-framework instaled
similar to https://github.com/ldoktor/fedora-avocado
Usage ::
```
$ avocado run sleeptest.py --docker debian-avocado
```

## xfstests-bld
**xfstests-bld**: xfstests-bld/Dockerfile
Base debian image with all necessary packages to build xfstests-bld from scratch.
**TODO**: Submit fixe