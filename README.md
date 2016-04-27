Laanwj's Bitcoin Core repository
==================================

In progress
-------------

### Database experiments

- [2016_04_mdb](https://github.com/laanwj/bitcoin/tree/2016_04_mdb)
  LMDB experiment - change UTXO and block index DB to use LMDB (aka "Symas
  Lightning Memory-Mapped Database") instead of LevelDB.

- [2016_04_dummy_db](https://github.com/laanwj/bitcoin/tree/2016_04_dummy_db)
  Dummy database experiment - This replaces the block index and UTXO
  database with an in-memory data structure which is read from disk at start,
  and written to disk at shutdown. There are no intermediate flushes.

- [2016_04_leveldb_sse42_crc32c_test](https://github.com/laanwj/bitcoin/tree/2016_04_leveldb_sse42_crc32c_test)
  Use SSE4.2 CRC32C instructions in LevelDB. LevelDB uses this cyclic redundancy check for integrity
  verification. See also [crcbench](https://github.com/laanwj/crcbench), to see the difference
  in raw throughput.

Ready for review
--------------------

- [2016_04_i18n_unicode_rpc](https://github.com/laanwj/bitcoin/tree/2016_04_i18n_unicode_rpc)
  add full UTF-8 support to RPC (and the underlying JSON implementation). See also
  [PR #7892](https://github.com/bitcoin/bitcoin/pull/7892) and upstream
  [PR #22](https://github.com/jgarzik/univalue/pull/22).

  - See also: [Univalue fuzzing branch](https://github.com/laanwj/univalue/tree/2015_11_unifuzz),
    and [instructions](https://gist.github.com/laanwj/68551528b7ae641ccaeb519566ca67c7) for building
    univalue with afl-fuzz.

Documents and notes
--------------------

- [Reducing bitcoind memory usage](https://gist.github.com/laanwj/efe29c7661ce9b6620a7).

Scripts
--------

- [Start bitcoind in a screen in a debugger](https://gist.github.com/laanwj/29bc141fb8d10608651c).
- [Measure compilation speed](https://gist.github.com/laanwj/108877a28ec03836568a) as well
 as other statistics such as maximum memory usage per compilation unit. Original
 [PR #6658](https://github.com/bitcoin/bitcoin/issues/6658#issuecomment-144643696).

