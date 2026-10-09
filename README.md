# Driftless for ZimaOS and CasaOS

App store source for [Driftless](https://projects.datapad.nl/docs/driftless), a
self-hosted file sync server by Datapad B.V.

## Add this store

In the App Store, add a community store and paste the address for your system.

ZimaOS:

```text
https://datapad-nl.github.io/driftless-zimaos/store.json
```

CasaOS:

```text
https://github.com/Datapad-nl/driftless-zimaos/archive/refs/heads/main.zip
```

Then search for **Driftless** and install it.

To install without adding a store, use **Custom install ▸ Import** and paste
[`Apps/Driftless/docker-compose.yml`](Apps/Driftless/docker-compose.yml).

## After installing

Open Driftless from the dashboard and create the administrator account. Add a
user for each person, then sign in from the desktop app with
`http://<your ZimaOS address>:8642` as the server.

The image is `ghcr.io/datapad-nl/driftless` (amd64 and arm64). Data is kept in
`/DATA/AppData/driftless/data`.

## How it is published

`Apps/` is the source. On every push to `main`, the `publish` workflow builds it
with IceWhale's `build-appstore-action` into the v2 format ZimaOS reads
(`store.json`, `index.json`, per-app compose and metadata) and deploys that to
GitHub Pages. CasaOS reads the branch zip directly.

## License

AGPL-3.0. See [LICENSE](LICENSE).
