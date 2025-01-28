# Go Concurrency Bug: Race Condition

This repository demonstrates a common concurrency bug in Go: a race condition when incrementing a shared variable from multiple goroutines.  The `bug.go` file contains code that exhibits this race condition, leading to inconsistent and unpredictable results. The `bugSolution.go` file presents a corrected version utilizing proper synchronization mechanisms.

## Bug Description

The `bug.go` program uses goroutines to increment a shared counter (`count`). Without proper synchronization, multiple goroutines can simultaneously access and modify `count`, leading to data races and incorrect final values.

## Solution

The `bugSolution.go` file addresses the race condition by using a `sync.Mutex` to protect the shared counter. This ensures that only one goroutine can access and modify `count` at a time, preventing data races and producing a consistent and correct result.