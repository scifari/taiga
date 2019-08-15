# Taiga

## Introduction

Taiga is a web application server that bundles Webification (w10n) software packages, such as [Pomegranate](https://github.com/scifari/pomegranate), for easy and efficient use of large and complex data in various formats (e.g., HDF4/5 and NetCDF, etc.)

## Installation

### Use docker image
The easiest way to install Taiga is to use a docker image, which is available at

https://hub.docker.com/r/scifari/taiga

### Use release tar ball

On CentOS or similar Linux distributions, you can check out or download most recent release from

https://github.com/scifari/taiga/tree/master/release

then install and configure as, e.g.,

```
$ mkdir  ./tool
$ cd ./tool
$ wget https://raw.githubusercontent.com/scifari/taiga/master/release/taiga-2.0.4p8-linux-x86_64.centos-7.5.1804-a.tar.gz
$ tar zxf ./taiga-2.0.4p8-linux-x86_64.centos-7.5.1804-a.tar.gz
$ ./taiga-2.0.4p8-linux-x86_64.centos-7.5.1804-a/bin/taiga-service config --port ${myPort} --dataDirectory ${myDataDirectory}
$ ./taiga-2.0.4p8-linux-x86_64.centos-7.5.1804-a/bin/taiga-service start -f 9
```
where `${myPort}` and `${myDataDirectory}` must be replaced by real values.

## Quick Start

After a successful install of Taiga,
one should be able to access w10n-sci web service,
via URLs in declarative style, using any http-aware client.

Two types of data stores are webified through Taiga:

* Directories on host's file system.
  Please check [use w10n store](./doc/w10n.md) for detailed URL syntax.
* Data files in HDF4/5 and NetCDF.
  Please check [use w10n-sci store](./doc/w10n-sci.md) for detailed URL syntax.

### A simple browsing GUI

Installed with Taiga is a simple html-based GUI,
that one can use to browse through w10n entities, namely,
directories and groups as nodes, files and arrays as leaves, etc.

Shown below are screenshots that illustrate this simple GUI,
using MillionSoundSample as an example. Please check [this doc](./doc)
for how to load MillionSoundSample data tarball to Taiga.

Assuming Taiga is started on `18080` of `localhost`, point browser to
`http://localhost:18080`, one should be able to see a `Welcome` page as

![page top](./figure/0-top.jpg)

Click on link `/data`, a page with a list of directories will be shown.
One directory is `MillionSongSample`.

![page data dir](./figure/1-data-dir.jpg)
