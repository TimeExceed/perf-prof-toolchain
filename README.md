# Toolchain to perf a Rust/C++ binary

## Prerequisites

1.  install `perf`

    ```console
    $ sudo apt-get install -y linux-tools-common linux-tools-generic
    ```

## Steps

1.  rebuild the project with debug info

    *   For Rust, add `debug = true` in the `[profile.release]` section.
    *   For C++, add `-g` for release build.

1.  profile with `flamegraph`

    ```console
    $ sudo /path/to/flamegraph -- ${EXECUTABLE_AND_ARGS}
    ```

## References

*   [Flame Graphs in main page of Brendan Gregg](https://www.brendangregg.com/flamegraphs.html)
*   [Repository of Flame Graphs from Brendan Gregg](https://github.com/brendangregg/FlameGraph)
*   [One single command implemented by Rust](https://github.com/flamegraph-rs/flamegraph)
