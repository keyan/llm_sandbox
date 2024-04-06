Quick notes on overall takeaways from several key LLM research papers

---------

# qlora: efficient finetuning of quantized llms 2023

- may have helpful background for my finetuning experiments
- doesn't use rl, but can we use rl w/ qlora? first thought is no, this only applies to supervised transformer training

---------

# language models are few-shot learners

- introduces gpt3 but not an interesting paper really for me
- model architecture is the same as for gpt2 and the paper just discusses different emperical testing procedures for evaluating how gpt3 is more capable
- provides evidence about scaling laws, an important research finding, but not much value for an implementer

---------

# constitutional ai: harmlessness from ai feedback

- offers the ‘rl from ai feedback’ (rlaif) solution as a way to train harmless lms without needing large volumes of human labeling, which is a big weakness of rlhf

---------

# Improving Language Understanding by Generative Pre-Training

https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf

- Most important paper on modern LLM workings
- The original GPT paper which introduces the semi-supervised approach
- Actually very surprising that this was the first time the unsupervised language modeling objective was used on unlabeled data with transformers, did BERT use labeled data?
- not sure why the decoder-only arch changes the model behavior, except that it prevents bidirectional attention (can only look backwards)
- originally trained on only 5GB of text

---------

# Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback

https://arxiv.org/pdf/2204.05862.pdf

- anthropic's version of instructgpt
- todo

---------

# Training language models to follow instructions with human feedback

https://arxiv.org/pdf/2203.02155.pdf

- instructgpt
- todo
