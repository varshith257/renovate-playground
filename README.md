# Renovate Playground

This is a minimal Go HTTP server demonstrating a vulnerable dependency. It uses `github.com/gorilla/mux@v1.8.0` [CVE-2021-44503](https://nvd.nist.gov/vuln/detail/CVE-2021-44503) and provides:

- `GET /` → returns "Welcome to the file server!"  
- `GET /files/{file}` → echoes back the requested `{file}` name  
- `GET /health` → returns `{"status":"ok"}` as JSON  

## How to run

```bash
go run main.go
```

## Dependency & Vulnerability

- **Module:** `github.com/gorilla/mux v1.8.0`  
- **Vulnerability:** Path traversal in route variables → [CVE-2021-44503](https://nvd.nist.gov/vuln/detail/CVE-2021-44503)

