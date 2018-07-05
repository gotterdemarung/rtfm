
# Profiling

Tools:
 - [Graphviz](http://www.graphviz.org) - `brew install graphviz` - to visualize profiling data

Go packages
 - [pprof](https://github.com/google/pprof) - profiling data visualizer - `go get -u github.com/google/pprof`


```bash
go test -bench=. -cpuprofile cpu.prof
go tool pprof -svg cpu.prof > cpu.svg
```

```bash
go test -bench=. -trace trace.out
go tool trace trace.out
```

# Race detection

`go test -race`
