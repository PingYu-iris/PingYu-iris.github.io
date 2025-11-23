---
layout: page
permalink: /publications/
title: publications
description: Publications organized by research topics
nav: false
nav_order: 1
---

## Improving LLM Reasoning Ability

**Moving Beyond Binary Verifiable Reward**  
Leitian Tao, Ilia Kulikov, Jason Weston, Ping Yu  
*2025* [Upcoming]

Current research on reasoning tasks mainly focuses on verifiable rewards. We studied whether using verifiable answers for GRPO can help with hard-to-verify reasoning tasks, and explored whether including hard-to-verify training data is necessary. We proposed combining reward model signals with rule-based signals for model training, which allows the reward signal to account for intermediate reasoning steps while avoiding the issue of reward hacking that arises when relying solely on reward models.

---

**Distilling System 2 into System 1**  
Ping Yu, Jing Xu, Jason Weston, Ilia Kulikov  
*2024* [[PDF](link)]

Investigate self-supervised methods to 'compile" (distill) higher quality outputs from System 2 techniques back into LLM generations without intermediate reasoning token sequences, as this reasoning has been distilled into System 1.

---

## Data Quality Improvement & Synthetic Data Generation

**CoT-Self-Instruct: Building high-quality synthetic prompts for reasoning and non-reasoning tasks**  
Ping Yu, Jack Lanchantin, Tianlu Wang, et al.  
*2025* [[PDF](link)]

Proposed CoT-Self-Instruct, a synthetic data generation method that uses Chain-of-Thought reasoning and automatic filtering to create high-quality training data. Achieves state-of-the-art results on verifiable reasoning benchmarks (MATH500, AMC23, AIME24, GPQA-Diamond) and surpasses human and standard Self-Instruct data on AlpacaEval 2.0 and Arena-Hard.

---

**RIP: Better models by survival of the fittest prompts**  
Ping Yu, Weizhe Yuan, et al.  
*ICML 2025* [[PDF](link)]

Proposed Rejecting Instruction Preferences (RIP), a data filtering method that evaluates training prompts via rejected response quality and reward gap between chosen/rejected outputs. Achieved large gains in model performance: +9.4% AlpacaEval2, +8.7% Arena-Hard, +9.9% WildBench (Llama-3.1-8B); and boosted Llama-3.3-70B Arena-Hard accuracy from 67.5→82.9 (18th→6th place).

---

**Self-alignment with instruction backtranslation**  
Xian Li, Ping Yu, Chunting Zhou, et al.  
*ICLR 2024 (Oral)* [[PDF](link)]

Developed instruction backtranslation, a scalable method to train instruction-following LLMs by automatically generating and curating instruction–response pairs from web text.

---

## Self-Improvement

**ReStrain: Reinforcement with Self-Restraint training on Reasoning Tasks**  
Zhaoning Yu\*, Zhaolun Su\*, Haozhu Wang, Jason Weston, Ping Yu\*, Jing Xu\*  
*2025* [Upcoming]

Introduced RESTRAIN, a self-penalizing RL framework that transforms unlabeled data into training signals by penalizing overconfident or low-confidence rollouts while preserving promising reasoning chains. RESTRAIN integrates with policy optimization (e.g., GRPO) and achieves large gains on challenging reasoning benchmarks, narrowing the gap with supervised training.

---

**Shepherd: A critic for language model generation**  
Tianlu Wang\*, Ping Yu\*, Ellen Tan, et al.  
*2023* [[PDF](link)]

Introduced Shepherd, a 7B-parameter LLM tuned to critique and refine model outputs using a curated feedback dataset. Shepherd's critiques match or surpass those of larger models, achieving 53–87% win rates against competitive alternatives and rivaling ChatGPT in human evaluation.

---

## LLM as Judge

**J1: Incentivizing Thinking in LLM-as-a-Judge via Reinforcement Learning**  
Chenxi Whitehouse, Tianlu Wang, Ping Yu, et al.  
*2025* [[PDF](link)]

Introduced J1, a reinforcement learning approach for training LLM-as-a-Judge with verifiable rewards that incentivize reasoning and reduce bias. J1 outperforms all existing 8B/70B models (including DeepSeek-R1 distillations), surpasses o1-mini, and even beats R1 on some benchmarks, demonstrating stronger judgment ability through improved chain-of-thought reasoning.

---

**Self-taught evaluators**  
Tianlu Wang, Ilia Kulikov\*, Olga Golovneva\*, Ping Yu\*, et al.  
*2024* [[PDF](link)]

Proposed Self-Taught Evaluator, a synthetic-data approach for training LLM-as-a-Judge without human labels. Through iterative self-improvement with reasoning traces and judgments, improved LLaMA3-70B-Instruct from 75.4 → 88.3 on RewardBench, surpassing GPT-4 and matching top reward models trained with human preferences.

---

## Others

**Chameleon: Mixed-modal early-fusion foundation models**  
Chameleon team  
*2024* [[PDF](link)]

Developed Chameleon, a family of early-fusion token-based multimodal models for unified image–text understanding and generation. Chameleon achieves state-of-the-art results in image captioning, surpasses LLaMA-2 on text tasks, competes with Mixtral 8x7B and Gemini-Pro, and matches/exceeds much larger models like GPT-4V in human evaluations of long-form mixed-modal generation.

---

**OPT-IML: Scaling language model instruction meta learning through the lens of generalization**  
OPT team  
*2022* [[PDF](link)]

Developed OPT-IML Bench, a large benchmark of 2,000 NLP tasks for studying instruction-tuning decisions (task diversity, sampling, demonstrations, objectives). Using this framework, trained OPT-IML 30B and 175B, showing improved generalization across unseen categories, tasks, and instances, and significantly outperforming OPT on multiple benchmarks.