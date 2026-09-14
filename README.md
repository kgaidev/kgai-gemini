# kgai — Gemini CLI extension

Shared decision memory for AI dev teams, as a [Gemini CLI](https://github.com/google-gemini/gemini-cli)
extension. Your agent records the decisions behind your code — what changed, why, even the
dead ends you ruled out — recalls them before changing code, and syncs them across the team
without merge conflicts.

## Install

```bash
gemini extensions install https://github.com/kgaidev/kgai-gemini
```

A personal Google login is no longer eligible for the Gemini CLI — set a `GEMINI_API_KEY`
from [AI Studio](https://aistudio.google.com/apikey) (its free tier is enough). Gemini asks
before each `kg` command; allow `kg` in the workspace policy to stop the prompting.

On first session the extension installs the `kg` engine to `~/.kgai` (prebuilt binaries for
Linux and macOS; Windows via WSL). Then work normally — the agent recalls and records
decisions on its own. Query or record by hand with `/kg-ask`, `/kg-decision`, `/kg-history`.

## This repository is generated

This is a build output of the main project, **[kgaidev/kgai](https://github.com/kgaidev/kgai)** —
the same engine and hook scripts, packaged for Gemini's manifest, TOML commands, and
millisecond hook timeouts. File issues, read the source, and find the Claude Code and Codex
CLI versions there. Rebuilt from the main repo with `scripts/build-host-pkg.sh`.

## License

MIT — see [LICENSE](LICENSE).
