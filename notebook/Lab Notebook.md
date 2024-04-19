
[[2024-04-19]]

Goals:
- 1st pass of reading [DPO paper](https://arxiv.org/pdf/2305.18290.pdf)
- skim [ORPO paper](https://arxiv.org/pdf/2403.07691v2.pdf)
- finish part 5/8 karpathy lecture

Done:
- applied to FAR.AI tech lead job

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