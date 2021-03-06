# Release Nodes #

## 0.2.2 (2013-12-24) ##

* Fixed a bug that occurred when using the memory-mode in a multi-threaded
  application. When using a single `Reader` from multiple threads in memory-
  mode, the internal state of the object could become corrupt if you replaced
  the MaxMind database file on disk with another database file.

## 0.2.1 (2013-11-15) ##

* Fixed bug that caused an exception to be thrown when two threads created a
  `MaxMind.Db.Reader` object at the same time. This was fixed using a
  synchronization lock around the code that opens/creates the memory map. We
  recommend that you share a `Reader` object across threads rather than
  create one for each thread or lookup.

## 0.2.0 (2013-10-25) ##

* Changed namespace from `MaxMind.DB` to `MaxMind.Db` to conform with
  Microsoft's recommendations.
* Replaced custom `BigInteger` implementation with
  `System.Numerics.BigInteger`.
* Made `Metadata` an internal property on `Reader`.

## 0.1.0 (2013-10-22) ##

* Initial release
