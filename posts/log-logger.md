date: 2015-10-31

# Why log.Logger is not an interface

The Go stdlib has a struct [`log.Logger`](https://godoc.org/log#Logger).
You may be wondering why it is not an interface and here is why.

Before we proceed, let's assume for this post that `log.Logger`'s API is fine in
spite of lack of logging level.

In traditional programming languages, such as Java, the stdlib defines canonical
interfaces that others can implement. Go stdlib does that too, but only when it
is necessary, and the necessity is determined by whether the interface is
consumed by the stdlib. This is because Go interfaces are implemented by types
implicitly.

If you define `MyLogger` interface with the `log.Logger` methods you actually
need, `log.Logger` automatically implements it.

```go
type MyLogger interface {
  Print(v ...interface{})
}

var l MyLogger = log.New(os.Stderr, "", 0)
```

If a third-party library author wants to define an alternative implementation
for an existing std type, such as `log.Logger`, all she needs is to conform its
API (methods). Then their implementation automatically implements your
`MyLogger` too.

```go

// Package better is a better implementation of log.Logger
package better

type Logger struct {
}

func (l *Logger) Print(v ...interface{}) {
   //....
}

// other methods
```

Now instead of accepting `*log.Logger` parameters in your functions, you can
always accept the `MyLogger` interface. Both `log.Logger` and `better.Logger`
can be used as an argument.

```go
package main

import (
  "better"
  "log"
)

// Logger is a subset of log.Logger methods that we need.
type MyLogger interface {
  Print(v ...interface{})
}

func do(l MyLogger) {
  l.Print("doing...")
}

func main() {
  do(log.New(os.Stdout, "", 0))
  do(&better.Logger{})
}
```

It is a good idea to accept an interface as a parameter, rather than a concrete
type. This way you allow callers to pass any implementation.

Therefore there is no need to define a canonical interface for logger. The
canonical set of methods is already defined by the struct. Stdlib team avoid
defining interfaces for types that stdlib doesn't consume, because they cannot
extend them later.
