# Mutexes
Mutexes allow us to *lock* access to data. This ensures that we can control which goroutines can access certain data at which time.

Go's standard library provides us with a built-in implementation of a mutex with the `sync.Mutex` type and its two methods:

- `Lock()`
- `Unlock()`

Mutexes are powerful. Like most powerful things, they can also cause many bugs if used carelessly.

**Attempting to wrap my head around Mutexes in Go**

The standard library also exposes a `sync.RWMutex`. It has these methods:

- `RLock()`
- `RUnlock()`

The sync.RWMutex can help with performance if we have a read-intensive process. Many goroutines can safely read from the map at the same time (multiple RLock() calls can happen simultaneously). However, only one goroutine can hold a Lock() and all RLock()'s will also be excluded.