# Driftless for ZimaOS and CasaOS

App store source for [Driftless](https://projects.datapad.nl/docs/driftless), a
self-hosted file sync server by Datapad B.V.

## Add this store

In the ZimaOS or CasaOS App Store, add a source and paste:

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

## License

AGPL-3.0. See [LICENSE](LICENSE).
