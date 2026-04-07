# LLM Bias & Trustworthiness Evaluation — Phishing-Susceptible Users

Evaluating the bias, trustworthiness, and fairness of open-source Large Language Models (LLMs) in the context of phishing-susceptible users. Using the DecodingTrust framework as a methodological foundation, this study assesses how Zephyr-7B responds to phishing-related prompts across different demographic groups — including elderly users, financially anxious individuals, non-native English speakers, and time-pressured users.

**Research question:** Does Zephyr-7B respond differently — and potentially unfairly — to phishing scenarios based on the demographic characteristics of the user described?

---

## Methodology

Follows the evaluation methodology from the DecodingTrust framework (Wang et al., 2023), adapted for phishing-susceptible user contexts.

**Model:** Zephyr-7B (HuggingFace Inference API)  
**Evaluation dimensions:** Stereotype Bias · Fairness · Toxicity · Privacy & Security · Factuality · Ethical Reasoning

**Prompt design:** 15 prompts across 5 base phishing scenarios, each with 3 demographic variants. Demographic details are the only variable changed between variants — enabling direct fairness comparison.

---

## Demographics Studied

| Group | Characteristic |
|-------|----------------|
| Elderly (65+) | Low digital literacy, high trust |
| Non-English speakers | Language barrier, unfamiliar with local systems |
| Financially anxious | Urgency bias, fear of loss |
| Time-pressured | Reduced critical thinking under stress |
| Overly trusting | Low suspicion of authority figures |

---

## Tools & Libraries

- `transformers` — HuggingFace model inference
- `detoxify` — Toxicity scoring
- `pandas` — Data handling
- `matplotlib` / `seaborn` — Visualisation
- `huggingface_hub` — API authentication

---

## Reference

Wang, B., et al. (2023). *DecodingTrust: A Comprehensive Assessment of Trustworthiness in GPT Models.* NeurIPS 2023. https://arxiv.org/pdf/2306.11698
