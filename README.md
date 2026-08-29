# HarnessBench

HarnessBench is a tiny RLM harness evaluation lab.

It connects two ideas I have been studying:

- Prime-Agent-style RLM harnesses: persistent state, subagents, tools, files, and self-improvement loops.
- Terminal-Bench-style evaluation: resource calibration, task quality, verifier risk, and continuous benchmark maintenance.

The core idea is simple:

> An agent failure is not always a model failure.

Sometimes the harness forgot state, split work badly, used the wrong tool, hit a resource limit, or got misled by a weak verifier. HarnessBench visualizes those failure modes and turns them into concrete harness improvement ideas.

## What It Shows

- Interactive failure cases
- RLM timeline for each run
- Outcome, cost, harness risk, and eval signal
- Suggested harness improvement
- JSON-style run record
- Prime Agent + Terminal-Bench inspired architecture loop

## Demo Cases

- Context lost across a long repair
- Resource limit looks like reasoning failure
- Verifier reward hack
- Subagents split the work badly

## Run Locally

This is a static HTML prototype.

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Why This Exists

I wanted a first project that was not just another blog post. The goal is to show that I understand the connection between:

- how agent harnesses are built,
- how long-horizon agents fail,
- how benchmarks should measure those failures,
- and how those failures can become self-improvement signals.

## References

- [Prime Agent: A Self-Improving RLM Harness](https://arxiv.org/abs/2608.23552)
- [Prime Agent repo](https://github.com/PrimeIntellect-ai/prime-agent)
- [Terminal-Bench 4.0](https://www.tbench.ai/news/terminal-bench-4-0)
- [Terminal-Bench repo](https://github.com/harbor-framework/terminal-bench)
- [Continuous Benchmarks](https://www.tbench.ai/news/continuous-benchmarks)
