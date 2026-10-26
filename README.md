# VM Kapazitätsplaner

Web-App zur Planung von VM-Migrationen und Host-Kapazität.

## Start

```bash
npm install
npm run dev
```

Öffne http://localhost:1420

## Features

- Kunden mit VMs verwalten
- Host-Kapazität pro Cluster (Singlesite B/Z, ITBC)
- Migrations-Timeline mit Host-Einbau-Planung
- Export/Import (JSON)

## Release

Ein Tag `vX.Y.Z` (muss zur `version` in `package.json` passen) baut die App,
veröffentlicht das Container-Image `ghcr.io/somemarco/capamgmt:X.Y.Z` und legt
ein GitHub-Release mit dem statischen Build als `.tar.gz` an. Jeder Push auf
`main` aktualisiert das Image `:edge`.

```bash
podman run --rm -p '[::1]:8080:8080' ghcr.io/somemarco/capamgmt:edge
```
