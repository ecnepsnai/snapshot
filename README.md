> [!CAUTION]
> `github.com/ecnepsnai/snapshot` is deprecated and replaced by [git.ecn.io/ian/snapshot](https://git.ecn.io/ian/snapshot).
> All users should migrate to `git.ecn.io/ian/snapshot` for continued updates. Tag v1.0.0 is drop-in compatible copy of the
> last release of `github.com/ecnepsnai/snapshot`.

# snapshot

Package snapshot provides a way to collect information about a running go application.

# Usage

## Add to your Project

```bash
go get github.com/ecnepsnai/snapshot
```

## Basic Snapshot

A basic snapshot contains statistics about the memory and GC, the process, and the host system.

```go
stats := snapshot.Collect()
```

## Full Snapshot

A full snapshot contains all information in the basic snapshot, along with a full heap dump. The results are written to
a ZIP file at the specified path.

```go
err := snapshot.Full("debug.zip")
```
