# annasmazhar.github.io

Personal site and portfolio. **One static page — no build step, no trackers, no dependencies.**

Live site: <https://annasmazhar.github.io>

| File | What it is |
|---|---|
| `index.html` | The site. GitHub Pages serves this branch root, so `index.html` is the page. |
| `README.md` | This file — the written version of the portfolio. |

---

## The rule this is built to

> If a tool makes a claim, it should be able to prove it.

Every repo below ships its tests, an evidence file, and the failure modes it does *not* hide.
A tool that says "this factor is noise" has to show the gate that rejected it, not just assert it.

---

## Tools

| Repo | What it is | What it refuses to do |
|---|---|---|
| [factorproof](https://github.com/AnnasMazhar/factorproof) | Evidence-gated factor research: purged walk-forward CV with embargo, IC decay, Benjamini–Hochberg FDR across the whole factor family, deflated Sharpe per factor. | Refuses to promote a factor that does not clear its gate. MIT |
| [replayproof](https://github.com/AnnasMazhar/replayproof) | Offline regression testing for LLM agents: record a run once, replay it forever with **zero API keys**, assert tool-call contracts, gate token cost. | Refuses to call a change "safe" without a replay to compare against. MIT |
| [fitsproof](https://github.com/AnnasMazhar/fitsproof) | A calibrated cost model and an enforced memory budget in front of a from-scratch NumPy inference engine (KV cache, quantisation). | Says loudly that the model does not fit instead of OOM-ing silently at token 400. MIT |
| [pytest-duckdb](https://github.com/AnnasMazhar/pytest-duckdb) | Pytest plugin for SQL pipeline testing with DuckDB: load fixtures, run queries, snapshot results. | Zero config to get started; Python 3.9 to 3.13. MIT |
| [pyspark_mcp](https://github.com/AnnasMazhar/pyspark_mcp) | An MCP server for data engineers: SQL-to-PySpark transpilation, AWS Glue job generation, Spark optimisation. | Usable from any MCP client, not one vendor's harness. MIT |

Each repo's own README carries the install and run commands; nothing here can drift out of date
silently, because the repo is the source of truth.

---

## Merged upstream work

Pull requests merged into other people's repositories, verified against the GitHub API.
Stars are the live count at the time of writing — the number next to each upstream is the one
GitHub reports now, and the link goes to the PR itself.

| Upstream | PR | What it fixed | Upstream stars |
|---|---|---|---|
| [google/zx](https://github.com/google/zx/pull/1464) | [#1464](https://github.com/google/zx/pull/1464) | Skip `node:` protocol imports in `--install` | 45.8k |
| [teng-lin/notebooklm-py](https://github.com/teng-lin/notebooklm-py/pull/2262) | [#2262](https://github.com/teng-lin/notebooklm-py/pull/2262) | `source_delete` accepts multiple sources (bulk) | 20.2k |
| [aws/aws-cdk](https://github.com/aws/aws-cdk/pull/37815) | [#37815](https://github.com/aws/aws-cdk/pull/37815) | Restore `notifyDelayAfter` for PySpark and Scala Spark ETL jobs | 13.0k |
| [strands-agents/harness-sdk](https://github.com/strands-agents/harness-sdk/pull/4067) | [#4067](https://github.com/strands-agents/harness-sdk/pull/4067) | Text content block silently dropped when a `toolUse` is pending in the same block stop | 9.2k |
| [strands-agents/harness-sdk](https://github.com/strands-agents/harness-sdk/pull/4059) | [#4059](https://github.com/strands-agents/harness-sdk/pull/4059) | Context offloader preserved non-bytes image/document blocks | 9.2k |
| [strands-agents/harness-sdk](https://github.com/strands-agents/harness-sdk/pull/3955) | [#3955](https://github.com/strands-agents/harness-sdk/pull/3955) | LlamaCppModel yields trailing usage metadata chunk after `finish_reason` | 9.2k |
| [dlt-hub/dlt](https://github.com/dlt-hub/dlt/pull/4283) | [#4283](https://github.com/dlt-hub/dlt/pull/4283) | Add dot separator to `get_table_prefix_layout` when `{table_name}` terminates the layout | 6.1k |
| [dlt-hub/dlt](https://github.com/dlt-hub/dlt/pull/3928) | [#3928](https://github.com/dlt-hub/dlt/pull/3928) | Coerce double to decimal via `str()` to avoid IEEE 754 expansion | 6.1k |
| [Cygnux-Labs/Tracekit](https://github.com/Cygnux-Labs/Tracekit/pull/474) | [#474](https://github.com/Cygnux-Labs/Tracekit/pull/474) | Warn when a hand-wired framework is not the tested version | 727 |
| [exmergo/dex](https://github.com/exmergo/dex/pull/775) | [#775](https://github.com/exmergo/dex/pull/775) | Validate semantic YAML against MetricFlow's schemas | 136 |

Ten merged pull requests across seven upstream projects; **eight of them landed in repositories
with more than 6,000 stars** (zx, notebooklm-py, aws-cdk, harness-sdk, dlt).

---

## Numbers policy

Every figure on the site is checked against the GitHub API and against the repository it
describes. Where a number can drift — test counts, CI state, upstream star counts — the page
links to the live source instead of printing a figure that goes stale. If a number here is
wrong, the link next to it is where you can prove it.

---

Deploy: push to `main`. GitHub Pages serves the branch root.
