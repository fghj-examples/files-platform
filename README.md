# files-platform

Shared infrastructure for the [fghj](https://github.com/mlnja/fghj) `files`
example: one Redis that both `files-api` and `files-worker` depend on.

It publishes a single flow, `cache`. Other repos write
`depends_on: [platform/cache]` and get the same node, so there is one Redis
container per run however many repos ask for it.

## The tutorial

This repo is the example the [fghj tutorial](https://fghj.mlops.ninja/tutorial/)
builds, one chapter at a time. Each chapter it appears in is a tag, `ch5`
to `ch7`, and `main` is the finished repo.
