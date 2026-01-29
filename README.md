
# Compound-QA Dataset

## Overview

Compound-QA is a benchmark designed to evaluate LLM capabilities across three dimensions: **Knowledge**, **Reasoning**, and **Understanding**. Each dimension features five distinct question types, including *Factual-Statement*, *Cause-and-Effect*, *Hypothetical-Analysis*, *Comparison-and-Selection*, and *Evaluation-and-Suggestion*.



<!-- 示例图片位置 -->
![Non-compound vs Compound Questions](path/to/your_figure_examples.png)
*Examples of non-compound (left) and compound (right) questions: the former poses multiple questions across turns, while the latter combines them within a single turn.*


---

## Directory structure

The `data/` directory is organized by capability, with subdirectories for each question type.

```text
data/
├── Understanding/
│   ├── Factual-Statement/
│   ├── Cause-and-Effect/
│   ├── Hypothetical-Analysis/
│   ├── Comparison-and-Selection/
│   └── Evaluation-and-Suggestion/
├── Reasoning/
│   └── (Same structure as above)
└── Knowledge/
    └── (Same structure as above)
```
---

## Required fields for each record

Each data entry must include the following fields:

* `ID` — unique identifier 
* `context` — optional background or passage 
* `com_question` — compound question covering multiple sub-questions
* `com_reference` — reference answer covering all sub-questions

Example JSON record:

```json
{
  "ID": "xxx_1",
  "context": "<optional background or passage>",
  "com_question": "<compound question>",
  "com_reference": "<reference answer covering all sub-questions>"
}
```
---

## Citation

If you use the Compound-QA dataset or find our work useful, please cite our paper:

```bibtex
@misc{hou2024compoundqabenchmarkevaluatingllms,
      title={Compound-QA: A Benchmark for Evaluating LLMs on Compound Questions}, 
      author={Yutao Hou and Yajing Luo and Zhiwen Ruan and Hongru Wang and Weifeng Ge and Yun Chen and Guanhua Chen},
      year={2024},
      eprint={2411.10163},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2411.10163}, 
}
```

