# Ansys Granta MI

> Runs Ansys Granta MI through this assistant instead of you opening the Ansys application by hand — it looks up and manages material property data used across engineering designs. Needs Ansys Granta MI installed and licensed on this computer; the first time you use it, point it at your Ansys install folder.

The bundle zip (**49.5 MB**) is stored in this repository at **`d834e2fb-c2a2-4b7f-99dd-fe0237d2e3a5.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `d834e2fb-c2a2-4b7f-99dd-fe0237d2e3a5` |
| Status in registry | active |
| Bundle size | 49.5 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `ANSYS_ROOT` | `C:\ANSYS\v252\ansys_inc` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "server.py"
  ],
  "cwd": "__INSTALL_DIR__",
  "env": {
    "ANSYS_ROOT": "",
    "ANSYS_WORKDIR": "__INSTALL_DIR__",
    "AEDT_NO_GUI": "1"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `d834e2fb-c2a2-4b7f-99dd-fe0237d2e3a5.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
