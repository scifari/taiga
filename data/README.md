# Sample Data

Here are some sample datasets that can be used to test installation of [Taiga](https://github.com/scifari/taiga).

Using [MillionSongSample.tar.gz](./MillionSongSample.tar.gz) as an example, first download and unpack the dataset as

```
$ mkdir ~/data
$ cd ~/data
$ wget https://raw.githubusercontent.com/scifari/taiga/master/data/MillionSongSample.tar.gz
$ tar zxf ./MillionSongSample.tar.gz
```

Then, download Taiga, install and configure it with directory `~/data` 

```
$ mkdir  ~/tool
$ cd ~/tool
$ wget https://raw.githubusercontent.com/scifari/taiga/master/release/taiga-2.0.4p9-linux-x86_64.centos-7.5.1804-a.tar.gz
$ tar zxf ./taiga-2.0.4p9-linux-x86_64.centos-7.5.1804-a.tar.gz
$ ./taiga-2.0.4p9-linux-x86_64.centos-7.5.1804-a/bin/taiga-service config --port 18080 --dataDirectory ~/data
```
Lastly, run Taiga

```
$ ./taiga-2.0.4p9-linux-x86_64.centos-7.5.1804-a/bin/taiga-service start -f 9
```
Pointing browser to http://127.0.0.1:18080, you can browse the data set as illustrated in
[Quick Start](https://github.com/scifari/taiga/#quick-start).
