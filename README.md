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


## Method
<div align="center">
<img src=images\method.png>
</div>

## Quantitative Results
<div align="center">
<img src=images\quan.png>
</div>


## Qualitative Results
<div align="center">
<img src=images\qual.png>
</div>

## Installation

Coming soon.

## Acknowlegdements

This codebase is based on [LLaVA](https://github.com/haotian-liu/LLaVA), [Qwen-VL](https://github.com/QwenLM/Qwen-VL) and [FastV](https://github.com/pkunlp-icler/FastV). Many thanks to the authors for generously sharing their codes!
