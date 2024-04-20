[[2024-04-26]]

Goals:

[[2024-04-25]]

Goals:

[[2024-04-24]]

Goals:
- read illustrated transformer more closely, look at more detailed references too

[[2024-04-23]]

Goals:
- start GPT lecture karpathy 7/8
- watch [transformers lecture](https://www.youtube.com/watch?v=XfpMkf4rD6E&t=618s&ab_channel=StanfordOnline)
- re-read [GPT1 paper](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)
- skim illustrated transformer
- start GPT lecture karpathy 7/8

[[2024-04-22]]

Goals:
- leetcode
- complete karpathy lecture 6/8

Done:
- 

[[2024-04-19]]

Goals:
- 1st pass of reading [DPO paper](https://arxiv.org/pdf/2305.18290.pdf)
- skim [ORPO paper](https://arxiv.org/pdf/2403.07691v2.pdf)
- finish part 5/8 karpathy lecture

Done:
- some leetcode problems
- applied to FAR.AI tech lead job
- did a first pass read of DPO paper
	- [Umass lecture](https://www.youtube.com/watch?v=2dUSoco8r3U&ab_channel=MohitIyyer) has good detailed look
- skimmed a few others papers
- read huggingface rlhf overview
	- This overview is great, especially the literature section: https://huggingface.co/blog/rlhf
	- https://huggingface.co/blog/stackllama
	- learned about `peft` library which can be used for LoRA fine-tuning https://github.com/huggingface/peft
		- Good rule is ~1.5GB GPU RAM per B params to fine-tune with parameter adatation
	- LoRA lets us fit models in GPU but training is still slow, data parallelism chunks the training data, computers forward/backward on N GPUs, then merges results to average the gradients ![[Pasted image 20240419151846.png]]
- An even newer approach to training parallelization is FSDP [fully sharded data parallel](https://pytorch.org/blog/introducing-pytorch-fully-sharded-data-parallel-api/) - not sure how important this is for PEFT, I think it is only needed for full parameter FT
- 
[[2024-04-18]]

Goals:
- start part 5/8 karpathy lecture
- review some backprop notes
	- https://cs231n.stanford.edu/handouts/derivatives.pdf
	- https://colah.github.io/posts/2015-08-Backprop/

Done:
- reviewed backprop calculus notes
- worked through part of karpathy lecture 5/8
- watched live stanford [cs25 transformers](https://web.stanford.edu/class/cs25/) lecture from Nathan Lambert on alignment of LMs
	- A few big takeways:
		- lots going on in the finetuning world, looks like a good direction to keep working towards for me
		- rlhf is not dead, many-shot jailbreaking defies safety gains, but rlhf produces more useful models that users prefer, are better at conversation, better at math
		- DPO is an easier to implement and simpler algorithm for RLHF that I should at least look into and perhaps focus reimplementation efforts on (in lieu of PPO)
		- DPO does give some marginally worse results in model quality though

[[2024-04-17]]

- Talked with 80k hours career advisor
	- [notes][https://docs.google.com/document/d/1oFF3S5yO7fNWcvjggPB-q4aPnjxDl7NcgbKw8o8vlw8/edit?usp=sharing] from that session
	- broad takeaway was that I am on a reasonable path, continuing to learn is good
	- some advice that I should not hold off on applying totally (like I am), maybe select a few places to apply to early with more SWE-bent perhaps
	- focus on producing in public, currently been a challenge as I'm more focused on learning than project work
	- found the [jacob hilton curriculum](https://github.com/jacobhilton/deep_learning_curriculum?tab=readme-ov-file) which matches my interest and current plans well, will continue to reference this
- Signed up an AI alignment jam via https://www.apartresearch.com/sprints
	- The upcoming sprint/jam isn't a great match for my interests but the next ones are, looks like a good thing to try though scheduling is tough
- Learned about SPAR program and read through some mentor reqs from the ongoing session
	- next session (over summer) opens apps at EOM, which I plan to apply to
	- many mentors wanted experience with finetuning open source LLMs, so made a note to include this as area of focus for future projects
- Finished part3 of karpathy makemore series (video 4/8 total)
	- implemented batch norm on the MLP from prior lectures