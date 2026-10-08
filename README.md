# Compute in Transit 03 — Data Movement in LLM Inference

What an LLM serving system moves between GPUs, pools and storage, and which of those flows a compute-in-transit module could usefully work on: the KV hand-off between prefill and decode pools, KV tiering and prefix fetch (LMCache, Mooncake), query-aware KV selection (Quest, PRISM), ring attention, MoE all-to-all, weight streaming and confidential AI. Includes an interactive hand-off calculator (model, prompt length, link, compression ratio) and a candidate table against the series' five tests.

Topics: KV hand-off, KV tiering, Query-aware selection, Ring attention, MoE all-to-all, Confidential AI.

**Live site:** https://brendanjameslynskey.github.io/CiT_03_Data_Movement_in_LLM_Inference/

Part of the [Compute in Transit series](https://github.com/BrendanJamesLynskey/LLM_Hub_Compute_in_Transit). Every number comes from [analysis/results.md](https://github.com/BrendanJamesLynskey/LLM_Hub_Compute_in_Transit/blob/main/analysis/results.md), written by [analysis/cit_budget.py](https://github.com/BrendanJamesLynskey/LLM_Hub_Compute_in_Transit/blob/main/analysis/cit_budget.py), from [Disaggregated_Inference_Sim's recorded results](https://github.com/BrendanJamesLynskey/Disaggregated_Inference_Sim/blob/main/examples/results.md) (sections 14, 15, 21 and 24; illustrative coefficients), or from a cited source. Every concept used here is explained, with links, in the [series glossary](https://brendanjameslynskey.github.io/LLM_Hub_Compute_in_Transit/#glossary). Sister series: [Fourier Optics for Inference](https://github.com/BrendanJamesLynskey/LLM_Hub_Fourier_Optics_Inference), [LLM Inference Simulators](https://github.com/BrendanJamesLynskey/LLM_Hub_Inference_Simulators), [FHE Accelerator Simulators](https://github.com/BrendanJamesLynskey/FHE_Hub_Accelerator_Simulators).

Licence: CC BY 4.0.
