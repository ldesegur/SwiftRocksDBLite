# SwiftRocks

SwiftRocks is an extention of facebook's RocksDBLite project. It wraps Swift classes around the popular NoSQL DB on all Apple Devices. The product is packaged as a framework to be easily used by new or existing projects. 

RocksDBLite is a project focused on mobile use cases, which don't need a lot of fancy things we've built for server workloads and they are very sensitive to binary size. For that reason, we added a compile flag ROCKSDB_LITE that comments out a lot of the nonessential code and keeps the binary lean.

Some examples of the features disabled by ROCKSDB_LITE:
* compiled-in support for LDB tool
* No backupable DB
* No support for replication (which we provide in form of TransactionalIterator)
* No advanced monitoring tools
* No special-purpose memtables that are highly optimized for specific use cases
* No Transactions
