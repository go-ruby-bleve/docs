# go-ruby-bleve documentation

**Pure-Go (no cgo) MRI-faithful full-text search library — index Hash-shaped documents and run match/phrase/term/prefix/fuzzy/wildcard/regexp/range/boolean queries with scoring.**

`go-ruby-bleve/bleve` is a faithful, pure-Go (zero cgo) reimplementation of Ruby's `bleve`,
matching reference Ruby (MRI) behaviour. The module path is
`github.com/go-ruby-bleve/bleve`.

It is a **standalone, reusable** library importable by any Go program, and the
backend bound into [go-embedded-ruby](https://github.com/go-embedded-ruby/ruby)
by `rbgo` as a native module — the same pattern as
[go-ruby-yaml](https://github.com/go-ruby-yaml/yaml). The dependency runs the
other way: this library has **no dependency on the Ruby runtime**.

!!! success "Status: pure-Go, CGO=0, differential-tested"
    A faithful pure-Go port of Ruby's `bleve`, validated against reference Ruby, at 100%
    coverage, `gofmt` + `go vet` clean, CI green across the six 64-bit Go targets
    and three OSes.

## Install

```sh
go get github.com/go-ruby-bleve/bleve
```

## Repositories

| Repo | What it is |
| --- | --- |
| [`bleve`](https://github.com/go-ruby-bleve/bleve) | the library — Ruby's `bleve` in pure Go |
| [`docs`](https://github.com/go-ruby-bleve/docs) | this documentation site (MkDocs Material, versioned with mike) |
| [`go-ruby-bleve.github.io`](https://github.com/go-ruby-bleve/go-ruby-bleve.github.io) | the organization landing page (Hugo) |
| [`brand`](https://github.com/go-ruby-bleve/brand) | logo and brand assets |

## Principles

- **Pure Go, `CGO_ENABLED=0`** — trivial cross-compilation, a single static
  binary, no C toolchain.
- **Reference-faithful.** Behaviour matches reference Ruby (MRI), validated by a
  differential oracle rather than approximated.
- **Standalone & reusable.** No dependency on the Ruby runtime — the dependency
  runs the other way; `rbgo` binds this module.
- **100% test coverage** is the target, enforced as a CI gate, across 6 arches.

## Where to go next

- [Why pure Go](why.md) — why this slice of Ruby lives as a standalone,
  interpreter-independent Go library.
- [Reference](reference.md) — install, import path and the API reference.

Source lives at [github.com/go-ruby-bleve/bleve](https://github.com/go-ruby-bleve/bleve).
