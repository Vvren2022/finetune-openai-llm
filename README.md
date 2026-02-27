# OpenAI LLM Fine-Tuning Workflow

This repository contains a practical notebook-based pipeline for fine-tuning OpenAI chat models using custom JSONL datasets.

## What we implemented

- OpenAI API setup and client initialization
- Dataset loading from `data.jsonl` and `data2.jsonl`
- Format validation for chat-style training examples (`role`/`content` checks)
- Token counting and dataset health checks
- Training cost and token-limit awareness before job creation
- File upload to OpenAI Files API for fine-tuning
- Fine-tuning job creation with suffix and supervised hyperparameters
- Job status monitoring (`running`, `succeeded`, etc.)
- Post-training inference with a fine-tuned model

## Key project files

- `openai_api_and_finetuning_of_gpt_model (1).ipynb` – active notebook with full workflow
- `openai_api_and_finetuning_of_gpt_model.ipynb` – synced main notebook version
- `data.jsonl` – training data
- `data2.jsonl` – additional dataset used for checks/experiments

## Important note

`fine_tuned_model` is `None` until a fine-tuning job reaches `succeeded`. While jobs are `queued`, `validating_files`, or `running`, the final model name is not yet assigned.

## Outcome

This codebase provides an end-to-end template for preparing data, launching fine-tune jobs, tracking lifecycle states, and testing a resulting fine-tuned OpenAI model.

<img width="1693" height="877" alt="image" src="https://github.com/user-attachments/assets/2e101ebf-cf94-4d38-87c6-2b99fc672d55" />


