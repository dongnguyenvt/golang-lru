golang-lru
==========
This repo is hard-fork of github.com/hashicorp/golang-lru to add generic interface which only available on go 1.18+

This provides the `lru` package which implements a fixed-size
thread safe LRU cache. It is based on the cache in Groupcache.

Documentation
=============

Full docs are available on [Godoc](http://godoc.org/github.com/dongnguyenvt/golang-lru)

Example
=======

Using the LRU is very simple:

```go
l, _ := New[int](128)
for i := 0; i < 256; i++ {
    l.Add(i, nil)
}
if l.Len() != 128 {
    panic(fmt.Sprintf("bad len: %v", l.Len()))
}
```
