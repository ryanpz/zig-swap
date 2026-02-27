# zig-swap

zig-swap is a Zig and ZLS version manager. It downloads the Zig version specified in the first argument, along with the respective ZLS release, and activates them by creating symlinks in `$HOME/.local/bin`.

- Portable: zig-swap is written in POSIX `sh` and does not use any utility extensions
- Minimal required dependencies: curl
- Verifies archive signatures if [minisign](https://github.com/jedisct1/minisign) is installed
- Supports Linux and macOS
- Manages Zig 0.9.0 and above
- Locally persists versions to avoid re-downloads

## Usage Example

```sh
$ zig-swap 0.15.1
# download output...
$ zig version
0.15.1
$ zls --version
0.15.0
```

## Notes

- zig-swap only supports tagged release versions of Zig
- Ensure `$HOME/.local/bin` is in your `PATH`
- Releases are downloaded from the official mirrors ([https://ziglang.org](https://ziglang.org) and [https://builds.zigtools.org](https://builds.zigtools.org)), and are managed in `$XDG_DATA_HOME/zig-swap`

## License

MIT
