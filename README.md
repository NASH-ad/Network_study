# Network_study
This repo contains small network experiments in Go.

Server example:

- sources/serveur.go: main HTTP server with graceful shutdown, logging, and routes
- static/index.html: sample static file served at /static/

Run locally:

```bash
# run directly
go run ./sources

# or build and run
go build -o bin/server ./sources
./bin/server
```

Endpoints:

- GET / -> "Hello Web!"
- GET /health -> JSON {"status":"ok"}
- POST /echo -> echoes received JSON body
- GET /static/ -> serves files from ./static/

Shutdown: server supports graceful shutdown on SIGINT/SIGTERM (5s timeout).
