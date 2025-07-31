# Short-LVLM: Compressing and Accelerating Large Vision-Language Models by Pruning Redundant Layers [ACM MM' 25]
Although large vision-language models (LVLMs) have demonstrated impressive capabilities in multi-modal understanding and
reasoning, their practical applications are still limited by massive
model parameters and high computational costs. Recent efforts from
natural language processing (NLP) have shown the effectiveness
of layer pruning, offering a plausible training-free compression
solution. However, due to the modality divergence between vision and language, it is unclear whether these NLP techniques are
still effective in LVLMs. In this paper, we empirically prove that
directly applying these layer pruning methods to LVLMs is ineffective. Through extensive experiments, we find that non-essential
vision-language (VL) tokens and inter-layer feature gaps pose critical challenges to pruning layers in LVLMs. Based on these insights,
we propose a novel framework Short-LVLM that can utilize important VL tokens and mitigate the layer-wise feature gaps. Notably,
Short-LVLM not only achieves a superior trade-off between performance and efficiency but also exhibits several potential advantages,
i.e., training-free, model-agnostic, and highly compatible.

## Motivation
<div align="center">
<img src=images\compare.png>
</div>
 Comparison of different model pruning methods.
(a) The training-based pruning methods involve fine-tuning
the pruned models. (b) The layer pruning methods achieve
training-free model compression via a localize-then-prune
process. (c) Our paradigm focuses on using important tokens
for layer localization and bridging inter-layer feature gaps
via weight projection.

## Method
<div align="center">
<img src=images\method.png>
</div>
Overview of our Short-LVLM (SVL). Our Short-LVLM consists of two key designs: (a) Localizing redundant layers with
Token Importance Scores (TIS) and (b) Bridging inter-layer feature gaps via Subspace-Compensated Pruning (SCP).


## Quantitative Results
<div align="center">
<img src=images\quan.png>
</div>
Results of Short-LVLM under varying Pruning Ratios across different Model Architectures and Model Scales. Acc and
Speed denote the accuracy and samples per second, respectively.

## Qualitative Results
<div align="center">
<img src=images\qual.png>
</div>
 Qualitative results of Short-LVLM. The retained
layers are depicted in blue. The results demonstrate that
Short-LVLM can preserve the capacity of LVLMs even when
nearly half of the layers are removed.

## Installation

Coming soon.

## Acknowlegdements

This codebase is based on [LLaVA](https://github.com/haotian-liu/LLaVA), [Qwen-VL](https://github.com/QwenLM/Qwen-VL), [mPLUG-Owl2](https://github.com/X-PLUG/mPLUG-Owl)) and [Nullu](https://github.com/Ziwei-Zheng/Nullu). Many thanks to the authors for generously sharing their codes!
