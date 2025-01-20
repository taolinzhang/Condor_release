# Condor

[![arXiv](https://img.shields.io/badge/arXiv-2403.12881-b31b1b.svg)](https://arxiv.org/abs/)
[![license](https://img.shields.io/github/license/InternLM/opencompass.svg)](./LICENSE)

## ✨ Introduction  

[[🤗 HuggingFace Models](https://huggingface.co/internlm/)]
[[🤗 HuggingFace Datasets](https://hf.co/datasets/internlm/Condor-SFT-20K)]
[[📃 Paper](https://arxiv.org/abs/)]
<!-- [[🧰 OpenXLab](https://openxlab.org.cn/models/detail/OpenLMLab/)] -->
<!-- [[🌐 Project Page](https://internlm.github.io/)] -->

> The quality of Supervised Fine-Tuning (SFT) data plays a critical role in enhancing the conversational capabilities of Large Language Models (LLMs).
However, as LLMs become more advanced, 
the availability of high-quality human-annotated SFT data has become a significant bottleneck, 
necessitating a greater reliance on synthetic training data. 
In this work, we introduce \textbf{Condor}, 
a novel two-stage synthetic data generation framework that incorporates  \textbf{World Knowledge Tree} and \textbf{Self-Reflection Refinement} to produce high-quality SFT data at scale. 
Our experimental results demonstrate that a base model fine-tuned on only 20K Condor-generated samples achieves superior performance compared to % RLHF-trained 
counterparts. 
The additional refinement stage in Condor further enables iterative self-improvement for LLMs at various scales (up to 72B), 
validating the effectiveness of our approach. 
Furthermore, our investigation into the scaling for synthetic data in post-training reveals substantial unexplored potential for performance improvements, 
opening promising avenues for future research.

## 🦅 Condor

Condor is a two-stage data synthesis engine designed to generate high-quality data for supervised fine-tuning of large language models (LLMs). The human-preference performance of the model improves significantly when fine-tuned with Condor, without affecting the model's knowledge capacity. The Condor pipeline is divided into two stages: data synthesis and data refinement. InternLM3 

- **Condor Void (Data Synthesis):**

    During the data synthesis stage, Condor introduces the \textbf{World Knowledge Tree}, which serves as a foundation of tags for data generation. Next, we apply task and difficulty expansion to enhance the diversity and complexity of questions under each tag, leading to the creation of the initial synthetic QA dataset.

- **Condor Refine (Data Refinement):**

    In the data refinement stage, Condor employs a \textbf{Self-Reflection Refinement} strategy, allowing the model to iteratively optimize the responses by generating new critiques and obtain the final refined dataset.




## 🤗 Datasets and Model Zoo 

The datasets and models are available on Huggingface.

|    Dataset    |                        Huggingface Repo                        |
| :---------: | :------------------------------------------------------------: |
| Condor Refine  | [Dataset Link](https://hf.co/datasets/internlm/Condor-SFT-20K)  |

|    Model    |                        Huggingface Repo                        |
| :---------: | :------------------------------------------------------------: |
| Condor-7B  | [Model Link](https://huggingface.co/internlm/)  |
| Condor-72B  | [Model Link](https://huggingface.co/internlm/)  |


## 🖊️ Citation

If you find this project useful in your research, please consider cite:
```
TODO
```

## 💳 License

This project is released under the Apache 2.0 [license](./LICENSE).
