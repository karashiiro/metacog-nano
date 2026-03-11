# metacog-nano

A lightweight MCP server implementing five metacognitive primitives as structured self-talk tools. Ported from [metacog](https://github.com/inanna-malick/metacog) to Rust using the [rmcp](https://github.com/modelcontextprotocol/rust-sdk) SDK with stdio transport.

## Build

```sh
cargo build --release
```

### Install

To install the binary to `~/.cargo/bin` (which is typically on your `$PATH`), run:

```sh
cargo install --path .
```

This lets you reference `metacog-nano` by name in MCP configs without needing a full path.

### Test

```sh
cargo test
```

## MCP Configuration

After installing with `cargo install --path .`:

```json
{
  "mcpServers": {
    "metacog-nano": {
      "command": "metacog-nano"
    }
  }
}
```

Or, if you prefer to reference the release binary directly without installing:

```json
{
  "mcpServers": {
    "metacog-nano": {
      "command": "/absolute/path/to/metacog-nano/target/release/metacog-nano"
    }
  }
}
```
