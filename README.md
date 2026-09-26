# EmbodiedSafe: Benchmarking Context-Aware Runtime Hazard Handling in Embodied Agents

EmbodiedSafe is a benchmark for evaluating context-aware runtime hazard handling in embodied agents. It contains four benchmark datasets with 1,480 samples, covers 77 safety mechanisms and 20 temporal safety obligations, and is grounded in 120 AI2-THOR scenes.

![EmbodiedSafe overview](figures/figure1.png)

## Safety knowledge

The `hazard_path/` directory contains the safety knowledge and its executable representation:

- [Embodied Safety Relation Graph](hazard_path/embodied_safety_relation_graph.html): links actions, predicates, safety mechanisms, hazards, and validated AI2-THOR instances.
- `actions.yaml`: action and interface definitions used to express executable task steps.
- `mechanisms.yaml`: safety-mechanism definitions with preconditions, trigger actions, effects, and hazard labels.
- `predicates.yaml`: predicate vocabulary and formal state tests used by the relation graph.

## Benchmark datasets

| Benchmark | Task | Contents |
|---|---|---|
| [Hazard Rejection](benchmark/hazard_rejection/README.md) | Reject instructions that would create hazards. | 900 records from 180 underlying tasks in five instruction forms. |
| [Context Sensitivity](benchmark/context_sensitivity/README.md) | Permit safe and block unsafe actions under matched contexts. | 240 records organized as 120 matched safe/unsafe pairs. |
| [Hazard Recovery](benchmark/hazard_recovery/README.md) | Complete a household task while restoring safety, or select a recovery plan. | 240 records: 120 execution cases and 120 plan-selection cases. |
| [Hazard Prospection](benchmark/hazard_prospection/README.md) | Complete tasks while meeting explicit or implicit safety deadlines. | 100 records from 50 temporal tasks in explicit and implicit versions. |

![Benchmark statistics](figures/figure2.png)
