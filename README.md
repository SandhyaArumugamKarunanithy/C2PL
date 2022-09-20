# C2PL
Locking-based concurrency control protocols use the concept of locking data items. A
lock is a variable associated with a data item that determines whether read/write
operations can be performed on that data item. Generally, a lock compatibility matrix is
used which states whether a data item can be locked by two transactions at the same
time.
Locking-based concurrency control systems can use either one-phase or two-phase
locking protocols. In a two phase locking method, all locking operations precede the
first lock-release or unlock operation. The transaction comprises two phases. In the first
phase, a transaction only acquires all the locks it needs and does not release any lock.
This is called the expanding or the growing phase. In the second phase, the transaction
releases the locks and cannot request any new locks. This is called the shrinking
phase. Every transaction that follows a two-phase locking protocol is guaranteed to be
serializable. However, this approach provides low parallelism between two conflicting
transactions.
