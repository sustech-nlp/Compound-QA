
# Compound-QA Dataset

**Summary**

Compound-QA is a benchmark designed to evaluate LLM capabilities across three dimensions: **Knowledge**, **Reasoning**, and **Understanding**. Each dimension features five distinct question types, including *Factual-Statement*, *Cause-and-Effect*, *Hypothetical-Analysis*, *Comparison-and-Selection*, and *Evaluation-and-Suggestion*.

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
  "ID": "pubmed_qa_1",
  "context": "<optional background or passage>",
  "com_question": "<compound question>",
  "com_reference": "<reference answer covering all sub-questions>"
}
```



