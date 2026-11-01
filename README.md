# AgentModelAgent

**An Agent that manages architecture search for the model stage of an Agent-native system.**

AgentModelAgent turns capability targets into architecture hypotheses, runs controlled ablations, and promotes only candidates supported by quality, memory, latency, and cost evidence.

用 Agent 托管模型架构研究：把能力目标转化为架构假设，执行受控消融，并依据质量、显存、延迟与成本证据推进候选方案。

## Agent loop

| Stage | Responsibility |
|---|---|
| Data | Task constraints, token budgets, compute envelopes, quality targets |
| Model | Tokenizer, attention, sparse routing, MoE, context, multimodality |
| Training | Small-scale probes and controlled ablations before scale-up |
| Inference | Memory, latency, and batching characteristics of candidates |
| Harness | Experiment schedulers, artifact stores, profiling, and rollback |
| Eval | Capability, scaling slope, memory footprint, latency, and cost |

## System contract

- Compare every candidate under the same resource envelope.
- Preserve rejected hypotheses and their measurements.
- Promote architecture choices from evidence, not fashion.

## Engineering principles

- Treat architecture as an empirical search space.
- Optimize the Pareto frontier instead of a single headline score.
- Carry evaluation failure slices into the next search cycle.

