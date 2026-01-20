# Numina-Lean-Agent

<div align="center">
  <a href=""><b>Paper</b></a> |
  <a href="https://leandex.projectnumina.ai"><b>Leandex</b></a> |
  <a href=""><b>Demo</b></a> |
  <a href="https://github.com/project-numina/Numina-Putnam2025"><b>Putnam 2025</b></a>
</div>

<br>

An agent built on Claude Code for Lean theorem proving tasks. We used this system to prove all 12 problems from Putnam 2025, and completed a paper-level formalization of [Effective Brascamp-Lieb inequalities](https://arxiv.org/abs/2511.11091).

## System Overview

<p align="center">
  <a href="assets/Numina-LeanAgent-v3.png">
    <img src="assets/Numina-LeanAgent-v3.png" alt="Numina-Lean-Agent system overview" width="900" />
  </a>
</p>


## Quick Start

### 1. Environment Setup

Follow the setup guide to install Lean, Claude Code, and numina-lean-lsp-mcp:

**[Tutorial: Setup Guide](tutorial/setup.md)**

### 2. Run Our Agent

See the usage guide for detailed instructions on running our agent:

**[Tutorial: Usage Guide](tutorial/usage.md)**

### Quick Example

```bash
# Run on a single file
python -m scripts.run_claude run leanproblems/Minif2f/mathd_algebra_478.lean \
  --prompt-file config/prompt_complete_file.txt \
  --max-rounds 5

# Run batch tasks from config
python -m scripts.run_claude batch config/config_minif2f.yaml

# Run all .lean files in a folder
python -m scripts.run_claude from-folder leanproblems/Minif2f \
  --prompt-file config/prompt_complete_file.txt \
  --max-rounds 5
```

## Related Projects

- [numina-lean-lsp-mcp](https://github.com/project-numina/lean-lsp-mcp) - MCP server for Lean LSP integration (based on [lean-lsp-mcp](https://github.com/oOo0oOo/lean-lsp-mcp))
- [lean4-skills](https://github.com/cameronfreer/lean4-skills) - Claude Code skills for Lean 4
- [Leandex](https://leandex.projectnumina.ai) - Semantic search for Lean codebases

## License

MIT License
