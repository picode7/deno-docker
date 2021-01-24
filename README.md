# Forked Deno Docker and Example

Forked from <https://github.com/hayd/deno-docker>

- Added `.vscode/settings.json` with deno extension config.
- Adjusted example and added docker instructions:

Build own container:

- make sure `_entry.sh` is in LF not CRLF [info](https://stackoverflow.com/questions/51508150/standard-init-linux-go190-exec-user-process-caused-no-such-file-or-directory)
- `docker build -f alpine.dockerfile -t deno-alpine .` (or user distribution)
- `cd example`
- `docker build -t deno-example .`
- `docker run -d -p 8080:1993 deno-example`
