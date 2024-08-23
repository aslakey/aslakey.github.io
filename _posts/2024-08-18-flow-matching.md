## Flow Matching for Generative Models

### [WIP]

Flow matching has been a primary ingredient for the significant improvements of generative models in 2024.  Stable Diffusion 3, FLUX, LuminaT2X, and many other models have recently incorporated this technique.  Similar to how [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239) (Jonathan Ho, et. al) popularized Gaussian diffusion, [Flow Matching for Generative Modeling](https://arxiv.org/pdf/2210.02747) is an accessible paper that suggests tangible, readily adoptable improvements for the current SOA generative image models. 

Yaron Lipman and team propose that a conditional, instance-level version of Continuous Normalizing Flows, coined Conditional Flow Matching, produces the same gradients as CNFs without the need for computationally expensive sumulations.  This unlocks the ability to train CNFs at modern scale.  They first show their Flow Matching derivations, employed with Gaussian diffusion paths, align with deterministic formulations found in [Maximum Likelihood Training of Score-Based Diffusion Models](https://arxiv.org/abs/2101.09258) by Song, et. al. Next, the propose departing from diffusion paths via Optimal Transport -- simpler, straight line trajectories between noise distribution and data distribution. 

In this post, I will review the core of Flow Matching for Generative Modeling alongside illustrative code snippets from LuminaT2X and graphics inspired by [this](https://www.youtube.com/watch?v=5ZSwYogAxYg) very informative presentation by Yaron Lipman.

---


