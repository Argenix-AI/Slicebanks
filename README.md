# SliceBank

**Persistent memory for large language models.**

SliceBank gives any LLM reliable long-term memory across conversations. Instead of forgetting what happened ten minutes ago, the model remembers — accurately — across dozens of sessions and hundreds of exchanges.

## Results

Tested on a 3B parameter model (Qwen2.5-3B-Instruct) against five baselines over 50 episodes (~400 queries):

| System | Overall Accuracy | Quality Index |
|---|---|---|
| **SliceBank** | **93.5%** | **94.3** |
| MemGPT | 48.8% | 32.8 |
| PromptWindow | 44.8% | 30.1 |
| RawContext | 40.9% | 27.2 |
| RAG | 15.1% | 14.9 |
| NoSlice | 4.1% | 8.0 |

In a shorter 16-episode evaluation, SliceBank scored **100%** with zero failures across 129 queries.

### Where the gap is widest

- **Retention** — SliceBank: 94.4%, best baseline: 8.1%
- **Rare information recall** — SliceBank: 96.3%, best baseline: 15.1%
- **Temporal reasoning** — SliceBank: 90.9%, all baselines: below 37%
- **Paraphrase & contradiction** — SliceBank: 100%

## Full Report

📄 **[SliceBank: Evaluation Results and Benchmark Comparison (PDF)](slicebank.pdf)**

## About

Built by Argenix
