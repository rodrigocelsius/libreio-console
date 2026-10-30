# libreio Console

The web management console for [libreio](https://github.com/rodrigocelsius/libreio),
a community-maintained fork of MinIO. This repository is a fork of the
MinIO Console (`github.com/minio/console`), licensed under the
**GNU AGPL v3.0**.

It is based on **MinIO Console v1.7.6**, the last release that ships the full
administration UI (users, groups, policies, identity providers, KMS,
configuration, events, tiers, logs, site replication, ...). Later upstream
versions reduced the console to an object browser only.

## Fork point

| | |
|---|---|
| Upstream | `github.com/minio/console` (removed from GitHub; history preserved via the [OpenMaxIO mirror](https://github.com/OpenMaxIO/openmaxio-object-browser)) |
| Upstream tag | `v1.7.6` (`f4a08fc0af8f776aa667677fb943aad137808f7c`) |
| Verification | Tree identical to the `v1.7.6` module zip served by `proxy.golang.org` |
| Git tag in this repo | `libreio-console-fork-point` |

## Usage

The console is embedded in the libreio server, which imports it as the Go
module `github.com/rodrigocelsius/libreio-console`. The compiled web
application lives in `web-app/build` and is embedded at build time.

To rebuild the web application (Node.js + Yarn 4):

```sh
cd web-app
yarn install
yarn build
```

The design system dependency (`mds`) is provided by
[libreio-mds](https://github.com/rodrigocelsius/libreio-mds).

## Documentation

The upstream README is kept at [docs/UPSTREAM_README.md](docs/UPSTREAM_README.md).

## Trademarks

MinIO is a trademark of MinIO, Inc. libreio is an independent project and is
not affiliated with, endorsed by, or sponsored by MinIO, Inc.

## License

GNU Affero General Public License v3.0; see [LICENSE](LICENSE) and
[NOTICE](NOTICE).
