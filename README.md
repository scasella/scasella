I study how language models reason and respond to training, and put AI agents to work on hard, checkable problems: formal proofs, faster code, real bugs.

Write-ups, models and every repo: **[casella.dev](https://casella.dev)**

## Research

Each write-up lists its model, data, code and open issues.

- **[Verified once, reused three times: agents carried proofs of shipped OpenSSL code into new callers](https://casella.dev/blog_reusable_binary_assurance.html)** · [sources](https://github.com/scasella/binary-proofs)<br>
  Machine-checked contracts for two unchanged Debian OpenSSL routines verified three experimental callers through their actual linkage. The held-out caller missed its three-hour cap, then completed in a recorded successor.
- **[Agents turned a one-kernel Lean proof into a checker that certified 25 PyTorch kernels](https://casella.dev/blog_certified_narrowing.html)** · [code](https://github.com/scasella/certified-int-narrowing)<br>
  One Lean theorem and a small checker certified 32-bit size arguments for 25 `torch.compile` kernels, including 10 of 24 held out, with each proof bound to the live compilation. Two of nine tuned kernels got faster.
- **[A Lean proof let agents cut a compiled PyTorch workload’s runtime by 26%](https://casella.dev/blog_pytorch_narrowing.html)** · [code](https://github.com/scasella/veritile-narrow-cat) · [PR](https://github.com/pytorch/pytorch/pull/198733)<br>
  Agents declared a `torch.compile` kernel’s size arguments 32-bit, proved in Lean when that is exact, and cut a changing-shape workload’s time by 26% on one L4.
- **[25 bugs in free-threaded CPython, found by agents](https://casella.dev/blog_cpython_ft.html)**<br>
  Agents confirmed 25 bugs in the no-GIL build, with no earlier report found for 18. TLAPS and Lean proofs of the locking model held; replays of real runs showed five places CPython leaves it.
- **[I used formal verification and agents to make an algorithm 105× faster and prove it behaves the same](https://casella.dev/blog_proof_optimizer.html)**<br>
  Seven rewrites of deliberately slow Dafny routines verified against a frozen spec; one ran 105× faster on a workload it never saw.
- **[A 50-step RL update reduces categorical sampling bias](https://casella.dev/blog_diversity.html)** · [code](https://github.com/scasella/research-uniform-random-from-llms)<br>
  Fifty RL steps on one random-integer task moved nine untrained pick-one tasks toward uniform on Qwen3-30B-A3B-Instruct.
- **[Hidden-state probes outperform self-reported confidence](https://casella.dev/blog_interp.html)** · [code](https://github.com/scasella/activation-probes-claim-correctness)<br>
  A linear probe on Llama 3.1 8B’s hidden states ranks claim correctness better than the model’s stated confidence.
- **[Panel-style reasoning trades accuracy for shorter completions](https://casella.dev/blog_multipersona.html)** and **[one RL run on sometimes-solvable problems](https://casella.dev/blog_multipersona_rl.html)** · [code](https://github.com/scasella/multi-model)

All eight: [casella.dev/research.html](https://casella.dev/research.html)

## Software

- **[Dynamic Workflows on Codex](https://github.com/scasella/claude-dynamic-workflows-codex)** — A Claude Code skill: describe a task, and Claude writes a multi-agent workflow script, runs it on Codex agents instead of Claude subagents, and shows the run as a live map.
- **[nanochat-mlx](https://github.com/scasella/nanochat-mlx)** — Train a small chatbot from scratch on Apple Silicon, from tokenizer training to a chat interface.
- **[Qwen Scope Lab](https://github.com/scasella/qwen-scope-lab)** — A browser workbench for sparse-autoencoder interpretability on Qwen3.5-2B, running on the Mac through MLX.

**ML on Apple Silicon:** [gemma4-m4-pro](https://github.com/scasella/gemma4-m4-pro) · [train-gemma4-sudoku-on-your-macbook](https://github.com/scasella/train-gemma4-sudoku-on-your-macbook) · [ttt-discover-autoresearch-mlx](https://github.com/scasella/ttt-discover-autoresearch-mlx)

**Research code:** [bsf-steering](https://github.com/scasella/bsf-steering) · [society-of-thought-bench](https://github.com/scasella/society-of-thought-bench) · [hypothesis_forge](https://github.com/scasella/hypothesis_forge) · [adaptive_rag_rlm](https://github.com/scasella/adaptive_rag_rlm) · [autoresearch-evo](https://github.com/scasella/autoresearch-evo) · [Proofgrade](https://github.com/scasella/Proofgrade)

**macOS menu bar apps** (TabPilot, SunShift, SafariMarkdown, GhostLabel, PasteForge, TextDrop and ClipDrop install with `brew install scasella/tap/<app>`, via [homebrew-tap](https://github.com/scasella/homebrew-tap)):
[TabPilot](https://github.com/scasella/TabPilot) · [SunShift](https://github.com/scasella/SunShift) · [SafariMarkdown](https://github.com/scasella/SafariMarkdown) · [GhostLabel](https://github.com/scasella/GhostLabel) · [PasteForge](https://github.com/scasella/PasteForge) · [TextDrop](https://github.com/scasella/TextDrop) · [ClipDrop](https://github.com/scasella/ClipDrop) · [DiskPulse](https://github.com/scasella/DiskPulse) · [PortSentry](https://github.com/scasella/PortSentry) · [ProcessBeacon](https://github.com/scasella/ProcessBeacon) · [BrewPilot](https://github.com/scasella/BrewPilot)

## Models

- [Random-choice adapter](https://huggingface.co/scasella91/qwen3-30b-a3b-answer-diversity-lora) — a Qwen3-30B-A3B LoRA for experiments with fixed-list sampling behavior.
- [Panel-reasoning adapter](https://huggingface.co/scasella91/qwen3-30b-a3b-multipersona-debate-lora) — the Qwen3-30B-A3B LoRA from the accuracy and completion-length comparison.

---

Personal projects. Not affiliated with or endorsed by my employer. Contact: [LinkedIn](https://www.linkedin.com/in/stevecasella/).
