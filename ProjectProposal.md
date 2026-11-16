# Project Proposal: Multilingual Safety Across Machine Translation

Gina Choi, Peter Huang

We propose to study how reliably LLM safety protections transfer across languages, **and whether translation quality contributes to observed safety gaps.** Specifically, we will evaluate whether harmful prompts refused in English produce different safety outcomes when translated into other languages, such as Korean and Swahili, **and whether these differences persist when the original intent is preserved.**

When AI jailbreak evaluations are written, they often focus on prompts in high-resource languages such as English, meaning users of less-resourced languages may encounter different safety protections. This problem is challenging because failures of safety, translation, and evaluation are often intertwined. **Our goal is to distinguish genuine cross-lingual safety failures from differences introduced by translation.**

We will primarily use **MultiJail**, which contains 315 harmful English prompts with parallel translations in nine other languages. We will compare its existing translations against machine-translated versions of the same prompts. **JailbreakBench's benign requests** will provide a control set to measure over-refusal.

Building on Deng et al. (2024), Wang et al. (2024), and Yong et al. (2023), we will evaluate two instruction-tuned LLMs, **Llama 3.1 and Qwen 2.5**, across English, Korean, and Swahili. We will measure **refusal rates, unsafe compliance rates, and semantic preservation**, comparing original, reference-translated, machine-translated, and back-translated prompts. **By analyzing cases where safety outcomes differ, we aim to determine how much apparent multilingual safety degradation may be explained by translation artifacts rather than language alone.**

## References

Deng, Y., Zhang, W., Pan, S. J., & Bing, L. (2024). *Multilingual Jailbreak Challenges in Large Language Models*. ICLR 2024.

Wang, W., et al. (2024). *All Languages Matter: On the Multilingual Safety of Large Language Models*. Findings of ACL 2024.

Yong, Z. X., et al. (2023). *Low-Resource Languages Jailbreak GPT-4*. arXiv:2310.02446.

Chao, P., et al. (2024). *JailbreakBench: An Open Robustness Benchmark for Jailbreaking Large Language Models*. NeurIPS 2024.