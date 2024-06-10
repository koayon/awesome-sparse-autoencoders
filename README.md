# Awesome Sparse Autoencoders

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Awesome Sparse Autoencoders is a curated list of papers,
models, explainers and libraries for Dictionary Learning With Sparse Autoencoders.

## Contents

- [Contents](#contents)
- [About](#about)
- [Architecture \& Theory](#architecture--theory)
- [Motivating Results](#motivating-results)
- [Safety Applications](#safety-applications)
- [Non-Safety Applications](#non-safety-applications)
- [Training Notes \& Intuitions](#training-notes--intuitions)
- [Open Source Libraries](#open-source-libraries)
- [AI Safety](#ai-safety)
- [Scaling Up \& Scaling Laws](#scaling-up--scaling-laws)
- [Trained Autoencoders](#trained-autoencoders)
- [Other](#other)

## About

`Dictionary Learning with Sparse Autoencoders (SAEs)` is a technique which ...

---

In this repo, links are organised by topic and have explanations so you can
decide what you would like to read. Especially recommended links are starred 🌟 and links which play a part in the current best recipe for SAEs are marked with a chef emoji 🧑‍🍳

Star this repository to see the latest developments in this research field.

We accept contributions! We strongly encourage researchers & practitioners to
make pull requests with papers, approaches and explanations that they feel
others in the community would benefit from 🤗

<!-- Ordered by topic, then date published -->

## Architecture & Theory

🧑‍🍳 🌟 **[TITLE], [LAB]: [AUTHORS] ([YEAR])**
[pdf]([LINK]),
[blog]([LINK]),
[code]([LINK]),
[demo]([LINK])

> [EXPLANATION]

🧑‍🍳 🌟 **Scaling Sparse Autoencoders, OpenAI: Gao et al (2024)**
[pdf](https://cdn.openai.com/papers/sparse-autoencoders.pdf)
[blog](https://openai.com/index/extracting-concepts-from-gpt-4/)
[code](https://github.com/openai/sparse_autoencoder)

> The OpenAI's Superalignment team (RIP) show that sparse autoencoders can be scaled to
> large models like GPT-4 and find some interesting features. The main contribution of
> this work though is the Top-K sparsity mechanism as an activation function which
> means that the l1 sparsity auxiliary loss is no longer needed.
>
> Their codebase is very clean but only shows using rather than training SAEs.
> Note their Triton kernels for sparse * dense matrix multiplication which improve
> the speed of training all SAEs - this is a great service to the community! (They use TransformerLens for
> activation caching).

🧑‍🍳 🌟 **Gated Sparse Autoencoders, DeepMind: Rajamanoharan et al (2024)**
[pdf](https://arxiv.org/pdf/2404.16014)

> To address the shrinkage problem in SAEs, DeepMind introduce a gating mechanism
> inspired by Shazeer-style GLUs. Theoretically this allows the autoencoder to separate
> predictions the magnitude of feature firing from whether the features fire or not.
> This seems to work and actually has benefits beyond what addressing shrinkage directly would
> do so it seems that the Gated SAEs also just provide better encoder representations.

## Motivating Results

## Safety Applications

## Non-Safety Applications

Linus - https://x.com/thesephist/status/1747099907016540181

Golden Gate Claude

## Training Notes & Intuitions

Circuits Updates Anthropic
Also DeepMind

## Open Source Libraries

🌟 **Dictionary Learning, Cavendish Labs: Ayonrinde et al (2023)**
[code](https://github.com/koayon/dictionary_learning)

> My favourite library for training sparse autoencoders.
> You can easily use lots of the different approaches to training SAEs and is
> designed to be a research library where you can define your own encoders, loss functions
> and activation functions. PRs are welcome!

**SAE Library, Eleuther: Belrose et al (2024)**
[code](https://github.com/EleutherAI/sae)

> A highly readable library for distributed training of sparse autoencoders with a great API interface.
> Mostly uses standard methods and isn't as customisable. More of a training library than a research one.

<!-- ## Multimodal -->

## AI Safety

<!-- Explainer -->

## Scaling Up & Scaling Laws

🌟 **Scaling Monosemanticity to Claude Sonnet, Anthropic: Templeton et al (2024)**
[website](https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html)
[blog](...)

> Anthropic show that the SAE approach scales to frontier scale models. A useful proof of concept
> and some interesting phenomenological results.
>
> There were a few criticisms of the paper [here] and [here]. # TODO: Add criticisms

## Trained Autoencoders

## Other

**Not All Language Model Features Are Linear, MIT: Engels et al (2024)**
[pdf](https://arxiv.org/pdf/2405.14860)

> SAEs generally lean on the Linear Representation Hypothesis. This paper shows that
> this is not always the case and that some features of language models are not linear.
> They show some examples of this for features which are essentially in low dimensional
> manifolds instead of being strictly linear and hypothesise that this could happen
> more widely. Very interesting work showing something that seemed to be the case and
> this shows that for the last few 9s of reliability we may need to think beyond strict linearity.
> They use SAEs to find the non-linear features.

🌟 **Automated Interpretability, OpenAI: Bills et al (2023)**
[website](https://openaipublic.blob.core.windows.net/neuron-explainer/paper/index.html)
[blog](https://openai.com/index/language-models-can-explain-neurons-in-language-models/)
[code](https://github.com/openai/automated-interpretability)
[forked code](https://github.com/hijohnnylin/automated-interpretability)

> Once you've trained your SAE typically you want to understand what it has learned
> by checking how interpretable the features are by humans or LLMs. This library allows you to do that
> and this work introduced the basic framework for automated interpretability.

<!-- ## Approaches We're Excited To See Explored More

-->

<br>

---

<br>

Thanks for reading, if you have any suggestions or corrections please submit a
pull request! And please hit the star button to show your appreciation.
