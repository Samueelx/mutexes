# Mutexes
Mutexes allow us to *lock* access to data. This ensures that we can control which goroutines can access certain data at which time.

Go's standard library provides us with a built-in implementation of a mutex with the `sync/Mutex` type and its two methods:

- `Lock()`
- `Unlock()`

Mutexes are powerful. Like most powerful things, they can also cause many bugs if used carelessly.
