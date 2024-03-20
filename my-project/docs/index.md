# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Codes

```
log:
  file: /var/log/lw_services/license_service.log
  level: info
  enableStdout: false

pgp:
  privateKey: LicenseServerKey/License_privateKey.sec
  publicKey: LicenseServerKey/License_publicKey.sec
  password: 12345600


# Only the first host will be taken
# TODO: support multiple hosts
services:
  lw-sentry:
    hosts:
      - host: 10.8.8.183:8087 #host or host:port
        httpsEnable: false
        skipTLS: true
  lw-auth:
    hosts:
      - host: 10.8.8.184:8090 #host or host:port
        httpsEnable: true
        skipTLS: true

db:
  redis:
    host: 10.8.9.50:6379
    password: 123456
  postgres:
    host: 10.8.9.50:5000
    username: licensedbapi
    password: 1234568
    dbname: licensedb
```
