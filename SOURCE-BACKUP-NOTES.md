# RoboRat® X MCP — Source Backup Notes

**Status:** Development-only source backup. NOT deployed, authenticated, or production-approved.

The original source package is named `x-chatgpt-mcp.tar.gz` (9,524 bytes).

## Integrity reference
- SHA-256: `adcea905711d424e597224e63589c64f24e0a2f7e2b6a299b02c88e4d5460d86`
- Git blob SHA-1 (for the original archive): `27d9867a5d56e02713b748697765ad19293307a0`

## Source archive contents
- `x_chatgpt_mcp/__init__.py`
- `x_chatgpt_mcp/config.py`
- `x_chatgpt_mcp/server.py`
- `x_chatgpt_mcp/x_client.py`
- `x_chatgpt_mcp/__main__.py`
- `README.md`, `requirements.txt`, `pyproject.toml`
- `.env.example`, `.gitignore`

## Security and operational notes
The package implements write-capable X tools, including `create_post` and `create_thread`. It currently has no server-enforced authenticated MCP caller validation, and its `dry_run` is not enforced by default. Do not publicly expose, deploy, or give it credentials without a separate security review. It does NOT replace the existing strictly read-only RoboRat® X Connector.

No real `.env` credentials, tokens, or keys were present in the reviewed archive. `.env.example` contains empty placeholders only.

Preserve the private repository's visibility. This document is a backup manifest, not evidence that the archive itself has been uploaded.
