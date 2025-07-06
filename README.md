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
