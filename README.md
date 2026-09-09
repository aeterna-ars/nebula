# Nebula

Nebula is a VPN protocol project focused on traffic masking and high-performance
packet processing. Its planned architecture combines a userspace handshake with
a kernel-space data plane.

**Status: early development.**

## Design direction

The project has two main goals:

- **Traffic masking:** make VPN traffic harder to identify and filter.
- **Efficient packet processing:** use a kernel-space data plane to handle traffic
  once a session has been established.

The handshake will run in userspace.

## Repository structure

- [nebula-core/](nebula-core/) — Rust crate, currently named `nebula-rs`.
- [nebula-go/](nebula-go/) — Go package, currently named `nebula_go`.

## Development

Requirements: Rust 1.85+ (edition 2024) and Go 1.24.4+.

Check the build:

```sh
(cd nebula-core && cargo check --locked)
(cd nebula-go && go build ./...)
```

## Contributing

Protocol design discussions, focused implementations, and test cases are welcome.
Please discuss substantial architectural changes in an issue before implementing
them.

## License

See [LICENSE](LICENSE) for the GNU General Public License, version 3.
