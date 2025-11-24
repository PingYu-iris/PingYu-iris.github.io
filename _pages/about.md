---
layout: about
title: home
permalink: /

profile:
  align: right
  image: about1.jpg
  image_circular: false

news: true
selected_papers: false
social: false
---

I am a Senior Research Scientist at [Meta FAIR](https://ai.meta.com/research/) in Seattle, working in [Jason Weston](https://scholar.google.com/citations?user=lMkTx0EAAAAJ&hl=en)'s research group. I focus on advancing the reasoning and alignment capabilities of large language models (LLMs).

My research interests focus on advancing the **reasoning** and **alignment** capabilities of large language models (LLMs). I have explored how to distill System-2 reasoning into LLMs, design alignment strategies such as training models to act as judges and integrating heterogeneous reward signals to improve GRPO, and develop methods for **LLM self-improvement** through iterative refinement. I am also interested in data-centric approaches, including generating and curating high-quality synthetic data to enhance pre-training and fine-tuning.

My current research focuses on **long-horizon credit assignment** for LLM-based agents and RL-trained models, particularly designing more informative and structured reward signals for agentic tasks with tool use and multi-step planning.

<div style="margin-top: 2rem;">
  <p><strong>📧 Contact:</strong> <a href="mailto:ping.yu.nlp@gmail.com">ping.yu.nlp@gmail.com</a> <em>(Updated)</em></p>
</div>

---

<h2 style="text-align: center; margin-top: 3rem; margin-bottom: 2.5rem; font-size: 2rem; font-weight: 300; color: #2c3e50;">Publications</h2>

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Improving LLM Reasoning Ability</h3>
</div>

**Hybrid Reinforcement: When Reward Is Sparse, It's Better to Be Dense**  
Leitian Tao, Ilia Kulikov, Swarnadeep Saha, Tianlu Wang, Jing Xu, Sharon Li, Jason Weston, <u>Ping Yu</u>.  
*2025* [[PDF](https://arxiv.org/pdf/2510.07242)]

Current research on reasoning tasks mainly focuses on verifiable rewards. We studied whether using verifiable answers for GRPO can help with hard-to-verify reasoning tasks, and explored whether including hard-to-verify training data is necessary. We proposed combining reward model signals with rule-based signals for model training, which allows the reward signal to account for intermediate reasoning steps while avoiding the issue of reward hacking that arises when relying solely on reward models.

---

**Distilling System 2 into System 1**  
<u>Ping Yu</u>, Jing Xu, Jason Weston, Ilia Kulikov.  
*2024* [[PDF](https://arxiv.org/abs/2407.06023)]

Investigate self-supervised methods to 'compile" (distill) higher quality outputs from System 2 techniques back into LLM generations without intermediate reasoning token sequences, as this reasoning has been distilled into System 1.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Exploring Data Quality Improvement & Synthetic Data Generation</h3>
</div>

**CoT-Self-Instruct: Building high-quality synthetic prompts for reasoning and non-reasoning tasks**  
<u>Ping Yu</u>, Jack Lanchantin, Tianlu Wang, Weizhe Yuan, Olga Golovneva, Ilia Kulikov, Sainbayar Sukhbaatar, Jason Weston, Jing Xu.  
*2025* [[PDF](https://arxiv.org/abs/2507.23751)]

Proposed CoT-Self-Instruct, a synthetic data generation method that uses Chain-of-Thought reasoning and automatic filtering to create high-quality training data. Achieves state-of-the-art results on verifiable reasoning benchmarks (MATH500, AMC23, AIME24, GPQA-Diamond) and surpasses human and standard Self-Instruct data on AlpacaEval 2.0 and Arena-Hard.

---

**R.I.P.: Better Models by Survival of the Fittest Prompts**  
<u>Ping Yu</u>, Weizhe Yuan, Olga Golovneva, Tianhao Wu, Sainbayar Sukhbaatar, Jason Weston, Jing Xu.  
*ICML 2025* [[PDF](https://arxiv.org/abs/2501.18578)]

Proposed Rejecting Instruction Preferences (RIP), a data filtering method that evaluates training prompts via rejected response quality and reward gap between chosen/rejected outputs. Achieved large gains in model performance: +9.4% AlpacaEval2, +8.7% Arena-Hard, +9.9% WildBench (Llama-3.1-8B); and boosted Llama-3.3-70B Arena-Hard accuracy from 67.5→82.9 (18th→6th place).

---

**Self-Alignment with Instruction Backtranslation**  
Xian Li, <u>Ping Yu</u>, Chunting Zhou, Timo Schick, Omer Levy, Luke Zettlemoyer, Jason Weston, Mike Lewis.  
*ICLR 2024 (Oral)* [[PDF](https://arxiv.org/abs/2308.06259)]

Developed instruction backtranslation, a scalable method to train instruction-following LLMs by automatically generating and curating instruction–response pairs from web text.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Self-Improvement</h3>
</div>

**RESTRAIN: From Spurious Votes to Signals -- Self-Driven RL with Self-Penalization**  
Zhaoning Yu, Will Su, Leitian Tao, Haozhu Wang, Aashu Singh, Hanchao Yu, Jianyu Wang, Hongyang Gao, Weizhe Yuan, Jason Weston, <u>Ping Yu</u>\*, Jing Xu\*.  
*2025* [[PDF](https://arxiv.org/abs/2510.02172)] (\* Equal contribution)

Introduced RESTRAIN, a self-penalizing RL framework that transforms unlabeled data into training signals by penalizing overconfident or low-confidence rollouts while preserving promising reasoning chains. RESTRAIN integrates with policy optimization (e.g., GRPO) and achieves large gains on challenging reasoning benchmarks, narrowing the gap with supervised training.

---

**Shepherd: A Critic for Language Model Generation**  
Tianlu Wang\*, <u>Ping Yu</u>\*, Xiaoqing Ellen Tan, Sean O'Brien, Ramakanth Pasunuru, Jane Dwivedi-Yu, Olga Golovneva, Luke Zettlemoyer, Maryam Fazel-Zarandi, Asli Celikyilmaz.  
*2023* [[PDF](https://arxiv.org/abs/2308.04592)] (\* Equal contribution)

Introduced Shepherd, a 7B-parameter LLM tuned to critique and refine model outputs using a curated feedback dataset. Shepherd's critiques match or surpass those of larger models, achieving 53–87% win rates against competitive alternatives and rivaling ChatGPT in human evaluation.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">LLM as Judge</h3>
</div>

**J1: Incentivizing Thinking in LLM-as-a-Judge via Reinforcement Learning**  
Chenxi Whitehouse, Tianlu Wang, <u>Ping Yu</u>, Xian Li, Jason Weston, Ilia Kulikov, Swarnadeep Saha.  
*2025* [[PDF](https://arxiv.org/abs/2505.10320)]

Introduced J1, a reinforcement learning approach for training LLM-as-a-Judge with verifiable rewards that incentivize reasoning and reduce bias. J1 outperforms all existing 8B/70B models (including DeepSeek-R1 distillations), surpasses o1-mini, and even beats R1 on some benchmarks, demonstrating stronger judgment ability through improved chain-of-thought reasoning.

---

**Self-Taught Evaluators**  
Tianlu Wang, Ilia Kulikov\*, Olga Golovneva\*, <u>Ping Yu</u>\*, Weizhe Yuan, Jane Dwivedi-Yu, Richard Yuanzhe Pang, Maryam Fazel-Zarandi, Jason Weston, Xian Li.  
*2024* [[PDF](https://arxiv.org/abs/2408.02666)] [[Model](https://huggingface.co/facebook/Self-taught-evaluator-llama3.1-70B)] (\* Equal contribution)

Proposed Self-Taught Evaluator, a synthetic-data approach for training LLM-as-a-Judge without human labels. Through iterative self-improvement with reasoning traces and judgments, improved LLaMA3-70B-Instruct from 75.4 → 88.3 on RewardBench, surpassing GPT-4 and matching top reward models trained with human preferences.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Others</h3>
</div>

**Chameleon: Mixed-modal early-fusion foundation models**  
Chameleon team.  
*2024* [[PDF](https://arxiv.org/abs/2405.09818)] [[GitHub](https://github.com/facebookresearch/chameleon)]

Developed Chameleon, a family of early-fusion token-based multimodal models for unified image–text understanding and generation. Chameleon achieves state-of-the-art results in image captioning, surpasses LLaMA-2 on text tasks, competes with Mixtral 8x7B and Gemini-Pro, and matches/exceeds much larger models like GPT-4V in human evaluations of long-form mixed-modal generation.

---

**OPT-IML: Scaling Language Model Instruction Meta Learning through the Lens of Generalization**  
OPT team.  
*2022* [[PDF](https://arxiv.org/abs/2212.12017)] [[Model-1.3B](https://huggingface.co/facebook/opt-iml-1.3b)] [[Model-30B](https://huggingface.co/facebook/opt-iml-30b)]

Developed OPT-IML Bench, a large benchmark of 2,000 NLP tasks for studying instruction-tuning decisions (task diversity, sampling, demonstrations, objectives). Using this framework, trained OPT-IML 30B and 175B, showing improved generalization across unseen categories, tasks, and instances, and significantly outperforming OPT on multiple benchmarks.

---

<div style="text-align: center; font-size: 2.5rem; margin-top: 3rem; margin-bottom: 2rem;">
  <a href="https://www.linkedin.com/in/ping-yu-05ba8212b" title="LinkedIn" target="_blank" style="margin: 0 1rem;"><i class="fab fa-linkedin"></i></a>
   <a href="https://scholar.google.com/citations?user=-V7TJhwAAAAJ" title="Google Scholar" target="_blank" style="margin: 0 1rem;"><i class="ai ai-google-scholar"></i></a>
  <a href="https://github.com/PingYu-iris" title="GitHub" target="_blank" style="margin: 0 1rem;"><i class="fab fa-github"></i></a>
</div>