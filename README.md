---
language: zh
---

# ERNIE-3.0-base-zh

## Introduction

ERNIE 3.0: Large-scale Knowledge Enhanced Pre-training for Language Understanding and Generation
More detail: https://arxiv.org/abs/2107.02137

## Released Model Info

This released pytorch model is converted from the officially released PaddlePaddle ERNIE model and 
a series of experiments have been conducted to check the accuracy of the conversion.

- Official PaddlePaddle ERNIE repo:https://paddlenlp.readthedocs.io/zh/latest/model_zoo/transformers/ERNIE/contents.html
- Pytorch Conversion repo:  https://github.com/nghuyong/ERNIE-Pytorch

## How to use
If you want to use ernie-3.0 series models, you need to add `task_type_id` to BERT model following this [MR](https://github.com/huggingface/transformers/pull/18686/files) 
**OR** you can re-install the transformers from my changed branch.
```bash
pip uninstall transformers # optional
pip install git+https://github.com/nghuyong/transformers@add_task_type_id # reinstall
```
Then you can load ERNIE-3.0 model as before:
```Python
from transformers import BertTokenizer, BertModel

tokenizer = BertTokenizer.from_pretrained("nghuyong/ernie-3.0-base-zh")
model = BertModel.from_pretrained("nghuyong/ernie-3.0-base-zh")
```

## Citation

```bibtex
@article{sun2021ernie,
  title={Ernie 3.0: Large-scale knowledge enhanced pre-training for language understanding and generation},
  author={Sun, Yu and Wang, Shuohuan and Feng, Shikun and Ding, Siyu and Pang, Chao and Shang, Junyuan and Liu, Jiaxiang and Chen, Xuyi and Zhao, Yanbin and Lu, Yuxiang and others},
  journal={arXiv preprint arXiv:2107.02137},
  year={2021}
}
```
