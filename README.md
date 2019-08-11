# Taiga

## Introduction

Taiga is a web application server that bundles Webification (w10n) software packages, such as [Pomegranate](https://github.com/scifari/pomegranate), for easy and efficient use of large and complex data in various formats (e.g., HDF4/5 and NetCDF, etc.)

## Installation

The easiest way to install Taiga is to use a docker image, which is available at

https://hub.docker.com/r/scifari/taiga

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

Please read [Use W10n store](./doc/w10n.md) and [Use w10n-sci store](./doc/w10n-sci.md)
