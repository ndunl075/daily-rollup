# daily-rollup

Reads click-stream CSV files, joins linked user IDs, builds sessions, credits ad clicks, and writes two daily Parquet tables.

- Language: Rust, standard library only. No third-party crates and no code from other projects.
- Build: `docker build .` (the build stage uses the official `rust` image from Docker Hub; the final image holds one static binary).
- Run: the container reads `$DATA_DIR`, writes `$OUTPUT_DIR/user_daily/` and `$OUTPUT_DIR/campaign_daily/`, and logs to stderr.

MIT licensed. See `LICENSE`.
