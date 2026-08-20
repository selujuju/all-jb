# AI Prompt Robustness Archive

![AI prompt research hero](assets/hero-ai-prompt-research.png)

A curated archive of prompt-injection, jailbreak, persona-conditioning, and response-format experiments collected across several language-model families.

> **Research collection, not a guarantee.** These files are preserved for controlled evaluation, red-teaming, and defensive research. Model behavior changes over time, and a prompt that appears effective in one environment may fail in another.

## Overview

This repository organizes experimental prompts that attempt to alter model behavior, override instruction hierarchies, impose unusual response formats, or expose differences between model configurations. The collection is intentionally preserved as a practical corpus for researchers, evaluators, and developers who want to study robustness rather than rely on anecdotal claims.

The archive currently contains **15 prompt files** spanning DeepSeek, Gemini, GLM, Grok, Kimi, Qwen, Sonnet, and ChatGPT-oriented experiments. Files are kept close to their original form so that provenance and reproducibility are not lost.

## Research themes

| Theme | What to look for | Related files |
| --- | --- | --- |
| Instruction hierarchy | Attempts to replace, reorder, or supersede higher-priority instructions | `3rd deepseek`, `better jb deepseek`, `deepseekjb.txt`, `grok jb` |
| Role and persona conditioning | Prompts that establish a persistent identity, voice, or behavioral frame | `glmjb`, `kimijb.md`, `qwen 3.8`, `sonnet 4.6 jb` |
| Response-format control | Strict prefixes, tags, line limits, narration rules, or structured output constraints | `deepseek thinking`, `deepseek v4`, `v sonnet 4.6(2nd)`, `qwen 3.8` |
| Cross-model variants | Similar patterns adapted for different model families or versions | `chatgptjb.txt`, `antigravity jb.txt`, `gem gemini 3.5 AND 3.6`, `glm 5.3` |
| Adversarial robustness | Prompts designed to test refusal boundaries, persistence, and resistance to conflicting directives | The full collection, evaluated only in authorized environments |

## Visual index

### Instruction hierarchy

![Instruction hierarchy](assets/instruction-hierarchy.png)

### Role conditioning

![Role conditioning](assets/role-conditioning.png)

### Output-format control

![Output-format control](assets/output-format.png)

### Reasoning-trace formatting

![Reasoning-trace formatting](assets/reasoning-traces.png)

### Adversarial override testing

![Adversarial override testing](assets/adversarial-overrides.png)

## File index

| File | Model or target | Format |
| --- | --- | --- |
| `3rd deepseek` | DeepSeek | Plain text |
| `antigravity jb.txt` | Antigravity | Plain text |
| `better jb deepseek` | DeepSeek | Plain text |
| `chatgptjb.txt` | ChatGPT | Plain text |
| `deepseek thinking` | DeepSeek | Plain text |
| `deepseek v4` | DeepSeek | Plain text |
| `deepseekjb.txt` | DeepSeek | Plain text |
| `gem gemini 3.5 AND 3.6` | Gemini | Plain text |
| `glm 5.3` | GLM | Plain text |
| `glmjb` | GLM | Plain text |
| `grok jb` | Grok | Plain text |
| `kimijb.md` | Kimi | Markdown |
| `qwen 3.8` | Qwen | Plain text |
| `sonnet 4.6 jb` | Sonnet | Plain text |
| `v sonnet 4.6(2nd)` | Sonnet | Plain text |

## Suggested evaluation workflow

Use an isolated test environment and record the model name, version, system configuration, sampling settings, date, prompt variant, and observed response. Compare results across repeated trials instead of treating a single successful or unsuccessful response as conclusive evidence.

For responsible testing, do not use these prompts to bypass safeguards on systems you do not own or have explicit permission to evaluate. Do not submit sensitive personal data, confidential documents, credentials, malware, or real-world operational targets to a model during experiments.

## Contributing

Additional files are welcome when they include enough context to preserve provenance: target model or version, date collected, source or author if known, and a short note describing the behavior being tested. Please avoid committing secrets, private data, or executable payloads.

## Disclaimer

This repository is an archival and educational resource. It does not endorse harmful, unlawful, deceptive, or unauthorized use. The maintainer and contributors make no claim that any prompt works, remains effective, or should be used outside an explicitly authorized evaluation environment.
