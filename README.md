# logging_utility_py

A **tiny, zero-dependency logger** that I reuse across all my Python micro-services and scripts.  
Version **0.1** is intentionally minimal—just a thread-unsafe singleton that prints timestamped messages to `stdout`.  
I’ll evolve it incrementally (JSON, context, middleware, etc.) and track progress in the Roadmap below.

---

## ✅ Current capabilities (v0.1)

| Feature | Notes |
|---------|-------|
| **Singleton** `Logger` | One global instance via `Logger.get_instance()` |
| **Five log levels** | `info`, `debug`, `warning`, `error`, `critical` |
| **Timestamped output** | `YYYY-MM-DD hh:mm:ss.mmm:LEVEL:message` |
| **Stdout sink** | No external libs or config—ideal for container logs |

---

## 🚀 Quick-start

```bash
# Clone repository then install in editable mode (for local tweaks)
git clone https://github.com/your-user/logging_utility_py.git
cd logging_utility_py && pip install -e .


from logging_utility_py.logger import Logger  # path will be updated once package is structured

log = Logger.get_instance()

log.info("Service starting…")
log.debug("Debug details here")
log.error("Something went wrong")


2025-07-06 12:34:56.123456:info:Service starting…
2025-07-06 12:34:56.123789:debug:Debug details here
2025-07-06 12:34:56.124012:error:Something went wrong
```

## 🛣️ Roadmap (planned)
 Thread-safe singleton (double-checked locking)

 - JSON / key-value log formatter

 - Correlation-ID context via contextvars

 - Colourised console output for local dev

 - Config via env vars or pyproject.toml

 - FastAPI / Flask middleware for request tracing

 - PyPI release once features are stable

Got ideas or want to help? Open an issue or a small PR—feedback welcome!
