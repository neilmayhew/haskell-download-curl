haskell-download-curl
=====================

*Debian packaging for the `download-curl` package from Hackage*

This repo contains only the `debian/` directory, and *not* the upstream sources.
It was forked from the now-discontinued Debian package of the same name, which
was part of the [DHG_packages][1] git repo and was removed in commit `ed54226`.

[1]: http://anonscm.debian.org/git/pkg-haskell/DHG_packages.git/

Building a package
------------------

First, ensure you have the necessary development tools installed:

```Bash
sudo apt-get install -y --no-install-recommends \
  devscripts fakeroot haskell-debian-utils \
  libwww-perl file
```

Then, download the upstream sources and unpack them:

```Bash
origtargz
```

(*Beware:* this also cleans the directory.)

You can now build a source package with:

```Bash
debuild -S -nc
```

To build the binary packages:

```Bash
sudo apt-get-build-depends -y
debuild -b
debuild clean
```
