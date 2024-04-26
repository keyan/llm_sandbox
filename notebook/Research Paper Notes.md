Quick notes on overall takeaways from several key LLM research papers

- [[#Direct Preference Optimization: Your Language Model is Secretly a Reward Model|Direct Preference Optimization: Your Language Model is Secretly a Reward Model]]
- [[#qlora: efficient finetuning of quantized llms 2023|qlora: efficient finetuning of quantized llms 2023]]
- [[#language models are few-shot learners|language models are few-shot learners]]
- [[#constitutional ai: harmlessness from ai feedback|constitutional ai: harmlessness from ai feedback]]
- [[#Improving Language Understanding by Generative Pre-Training|Improving Language Understanding by Generative Pre-Training]]
- [[#Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback|Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback]]
- [[#Training language models to follow instructions with human feedback|Training language models to follow instructions with human feedback]]
- [[#Fine-Tuning Language Models from Human Preferences|Fine-Tuning Language Models from Human Preferences]]

## Direct Preference Optimization: Your Language Model is Secretly a Reward Model

https://arxiv.org/pdf/2305.18290.pdf

[[2024-04-19]] first pass
- introduces DPO, alternative to RLHF that learns human preferences from preference data without using RL
- RLHF fits a reward model to preference data, then uses that rewards model to do RL and update the LM policy
- DPO directly optimizes a LM without explicit reward modeling or RL
- DPO optimizes the same objective as RLHF (reward maximization with KL-divergence constraint, not sure what this is?) but is easier to implement and train (both systems level and computationally less expensive)
- DPO uses clever math to define preference loss as a function of the policy directly, instead of using this to train RM

## qlora: efficient finetuning of quantized llms 2023

- may have helpful background for my finetuning experiments
- doesn't use rl, but can we use rl w/ qlora? first thought is no, this only applies to supervised transformer training

## language models are few-shot learners

https://arxiv.org/pdf/2005.14165

edit: [[2024-04-25]] - I think I missed the main finding here... the prior GPT papers didn't touch on the unique aspects of the transformer/GPT arch, that the "inner loop"/"in context learning" learns just from the prompt context, without explicit SGD like during pre-training. This is actually really bizarre because somehow the model is capable of meta-learning, perhaps the model weights are able to do some sort of SGD on the few-shot prompt examples just during a single forward pass. How? Why? We don't know.

- introduces gpt3 but not an interesting paper really for me
- model architecture is the same as for gpt2 and the paper just discusses different emperical testing procedures for evaluating how gpt3 is more capable
- provides evidence about scaling laws, an important research finding, but not much value for an implementer

## constitutional ai: harmlessness from ai feedback

- offers the ‘rl from ai feedback’ (rlaif) solution as a way to train harmless lms without needing large volumes of human labeling, which is a big weakness of rlhf

## Improving Language Understanding by Generative Pre-Training

https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf

- Most important paper on modern LLM workings
- The original GPT paper which introduces the semi-supervised approach
- Actually very surprising that this was the first time the unsupervised language modeling objective was used on unlabeled data with transformers, did BERT use labeled data?
- not sure why the decoder-only arch changes the model behavior, except that it prevents bidirectional attention (can only look backwards)
- originally trained on only 5GB of text

## Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback

https://arxiv.org/pdf/2204.05862.pdf

- anthropic's version of instructgpt
- todo

## Training language models to follow instructions with human feedback

https://arxiv.org/pdf/2203.02155.pdf

- instructgpt
- todo

## Fine-Tuning Language Models from Human Preferences

https://arxiv.org/pdf/1909.08593.pdf

[[2024-04-19]]
- Original paper on using RLHF w/ PPO for LM fine-tuning
- has all the methods and training detail needed for an RLHF reproduction
- experiments for evaluations use ROGUE as well as human comparison

---
### Neural Machine Translation By Jointly Learning To Align And Translate 
https://arxiv.org/pdf/1409.0473.pdf

[[2024-04-25]]
- precursor paper to "attention is all you need", first time self-attention is introduced
- section 3.1 has the most detail on the attention mechanism but I still find it hard to parse in isolation, finding clear comparison to modern transformer arch is challenging