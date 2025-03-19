[deepseek-v3-technical-report]: https://arxiv.org/abs/2412.19437

[deepseek-v3-leaderboard]: ../assets/deepseek-v3-leaderboard.png


[claude-official-website]: https://www.anthropic.com/news/claude-3-7-sonnet

[claude-technical-report]: https://assets.anthropic.com/m/785e231869ea8b3b/original/claude-3-7-sonnet-system-card.pdf

[claude-swe-bench-verified]: ../assets/claude-swe-bench-verified.webp

[HumanEval]: https://paperswithcode.com/sota/code-generation-on-humaneval
[HumanEval-paper]: https://arxiv.org/abs/2107.03374

[MBPP]: https://paperswithcode.com/sota/code-generation-on-mbpp
[MBPP-paper]: https://arxiv.org/abs/2108.07732

[LiveCodeBench-Base]: https://livecodebench.github.io/leaderboard.html
[LiveCodeBench-Base-paper]: https://arxiv.org/abs/2403.07974

[CRUXEval-I]: https://crux-eval.github.io/leaderboard.html
[CRUXEval-O]: https://crux-eval.github.io/leaderboard.html
[CRUXEval-paper]: https://arxiv.org/abs/2401.03065

[SWE-Bench]: https://www.swebench.com/#verified
[SWE-Bench-paper]: https://arxiv.org/abs/2310.06770

# State-of-the-Art Leaderboard

### [Code Performance][deepseek-v3-technical-report] Evaluation

![deepseek-v3-leaderboard]

| Benchmark            | Paper                                    | Metric | Few-shot | Supported Languages      | Description                                                              |
|----------------------|----------------------------|--------|----------|--------------------------|--------------------------------------------------------------------------|
| [HumanEval]          | [arXiv][HumanEval-paper]          | Pass@1 | 0-shot   | Python                   | Assessment of function implementation capabilities based on natural language specifications |
| [MBPP]               | [arXiv][MBPP-paper]               | Pass@1 | 3-shot   | Python                   | Evaluation of solutions to fundamental programming tasks with basic algorithmic complexity |
| [LiveCodeBench-Base] | [arXiv][LiveCodeBench-Base-paper] | Pass@1 | 3-shot   | Python, JavaScript, Java | Measurement of performance on complex, industry-relevant programming challenges |
| [CRUXEval-I]         | [arXiv][CRUXEval-paper]           | EM     | 2-shot   | Python, C++, Java        | Analysis of algorithm implementation quality specific to input processing mechanisms |
| [CRUXEval-O]         | [arXiv][CRUXEval-paper]           | EM     | 2-shot   | Python, C++, Java        | Evaluation of algorithmic efficiency and correctness in output processing functionalities |
| [SWE-bench]          | [arXiv][SWE-Bench-paper]          | Pass@1 | Varies  | Multiple (Based on Repo) | Evaluation of LLMs on real-world software engineering tasks, including bug fixes and feature implementation within existing codebases from various open-source projects.


<br>

### [Practical Code Performance][claude-official-website] Evaluation

![claude-swe-bench-verified]


<br>

### Metric Definition

[Pass@1-paper]: https://arxiv.org/abs/2107.03374
[Exact-Matching-paper]: https://arxiv.org/pdf/2203.13899


| Metric |         Definition | Focus |
|--------|--------------------|-------|
| [Pass@1][Pass@1-paper] | Measures the proportion of times a model generates code that passes all predefined test cases in a single attempt | Precision and probability of generating completely correct code in one try |
| [Test Pass Rate][SWE-Bench-paper] | Measures the proportion of times a model's generated code (often a code patch) passes all relevant tests in a real-world testing environment | Integration capability and performance in practical testing scenarios |
| [EM (Exact Matching)][Exact-Matching-paper] | Measures the proportion of times a model's output exactly matches the correct answer | Code reasoning and understanding capabilities |