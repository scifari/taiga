# How to Use Webification (w10n)

### File System Directory as Example

Scifari.org &copy; 2011 - 2019

W10n virtualizes an arbitrary data store as a tree, in which two types of entities exist: **node** and **leaf**.
A node can contain sub-nodes and leaves. A leaf holds data and is terminal. Both node and leaf can have attributes.

It employs meaningful URLs to locate inner components of a data store and make them directly accessible via HTTP/HTTPS in RESTful way.

A w10n URL has a form as follows

```
https://host:port/path/store/identifier?queryString
```

### File System Directory as W10n Store

When a file system directory is webified as a date store, its sub-directories become w10n nodes and files become w10n leaves.

By default, meta info, i.e., content of a directory is returned in HTML,

```
http://127.0.0.1:18080/data/MillionSongSample/
```

[link](http://127.0.0.1:18080/data/MillionSongSample/)

To have it in JSON, specify query parameter as `?output=json`, e.g.,

```
http://127.0.0.1:18080/data/MillionSongSample/?output=json
```

[link](http://127.0.0.1:18080/data/MillionSongSample/?output=json.indented)

Furthermore, one can use [glob](https://en.wikipedia.org/wiki/Glob_(programming)) pattern in URLs to filter the content, e.g.,

```
http://localhost:18080/data/Million*Sample/
```

[link](http://localhost:18080/data/Million*Sample/)

```
http://localhost:18080/data/Million*Sample/*ABC*12[89]*.h5/
```

[link](http://localhost:18080/data/Million*Sample/*ABC*12[89]*.h5/)

To have the response returned in JSON, specify query parameter as `?output=json`, e.g.,

```
http://localhost:18080/data/Million*Sample/?output=json
```

[link](http://localhost:18080/data/Million*Sample/?output=json.indented)

```
http://localhost:18080/data/Million*Sample/*ABC*12[89]*.h5/?output=json
```

[link](http://localhost:18080/data/Million*Sample/*ABC*12[89]*.h5/?output=json.indented)

### Further Reading

Many different types of data stores can be virtualized through w10n.
Please check [use w10n-sci](../../doc/w10n-sci/usage.md) for one important example.
