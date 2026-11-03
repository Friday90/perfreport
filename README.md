# PerfReport in Rust

IS2083 Advanced Scripting, Lab 3. This project migrates the original Windows-only
C++ PerfReport utility into Rust using `sysinfo` so it can run on Windows and Linux.

## Output

The program reports logical processors, total and free memory, memory use,
uptime, disk space and usage, and a 0-100 efficiency score. The score keeps
the rules from the original C++ version: memory above 70%/85% and disk above
75%/90% reduce the score by 10/25 points each.

## Run and test

From this folder in PowerShell:

```powershell
cargo fmt
cargo build --release
cargo run
cargo test
```

## Docker

With Docker Desktop running:

```powershell
docker build -t perfreport .
docker run --rm perfreport
```

## CI/CD

The `.github/workflows/ci.yml` workflow runs formatting checks, Clippy,
release build, and tests; the Docker image builds only after those checks pass.

## Notes

See `NOTES.md` for a short migration comparison and the AI assistance
disclosure required by the assignment.
