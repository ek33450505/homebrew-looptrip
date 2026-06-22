# homebrew-looptrip

Homebrew tap for [looptrip](https://github.com/ek33450505/looptrip) — a deterministic,
framework-agnostic detector of multi-agent coordination pathologies that trips at
**iteration 2, not on the invoice**.

## Install

```bash
brew tap ek33450505/looptrip
brew install looptrip
```

Then:

```bash
looptrip --version
looptrip proof          # reproduce the $792.96 hermetic proof on real recorded runaways
looptrip scan --all cast-db:<session_id>
```

## What it provides

- The `looptrip` CLI — `proof`, `scan` (duplicate-work, ping-pong / livelock, deadlock,
  non-termination), and `attribute` (counterfactual-replay attribution).
- Detection over OpenTelemetry GenAI handoff spans and a CAST `cast.db`.
- A deterministic, zero-LLM core (Python stdlib only). An **observer, never a gate** — it
  reports, it never blocks.

The formula installs from the published [PyPI sdist](https://pypi.org/project/looptrip/)
into an isolated virtualenv; the optional `[otel]` extra (the live `LooptripSpanProcessor`)
is not bundled — `pip install 'looptrip[otel]'` for that.

## Without Homebrew

```bash
pip install looptrip
```
