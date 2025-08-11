# Convex Schema Visualizer

Quick start
- Serve locally:
  - Python: `python3 -m http.server 8000 --bind 0.0.0.0 --directory /workspace`
  - Open: `http://localhost:8000/index.html`
- Public link (trycloudflare):
  - Download: `curl -L https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64 -o cloudflared && chmod +x cloudflared`
  - Run: `./cloudflared tunnel --url http://127.0.0.1:8000`
  - Copy the printed `https://*.trycloudflare.com` and open `/index.html`

Docker
```
# Build
docker build -t convex-schema-viz .
# Run
docker run -p 8000:8000 convex-schema-viz
# Open
http://localhost:8000/index.html
```

Features
- Graph view with draggable nodes and relationships from id(table) fields
- Inspector-based schema editing; JSON editor; validation; share links
- Functions builder with ReadTable, Filter, SelectFields, Join, SortBy, Limit
- LocalStorage persistence; import/export schema and functions