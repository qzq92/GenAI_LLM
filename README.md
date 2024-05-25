# GenAI_LLM
Repository containing example Jupyter notebooks provided by Coursera's Generative AI with LLM for their 3 labs. 

## Course Information
In Generative AI with Large Language Models (LLMs), you’ll learn the fundamentals of how generative AI works, and how to deploy it in real-world applications. The main LLM model used in this course is FLAN-T5 base model downloadable from HuggingFace, a model released by Google which is an instructioned fine-tuned version of T-5 Model (Text-To-Text Transfer Transformer), based on > 1800 language tasks, with increased reasoning skills and promptability. As for the dataset, HuggingFace's Dialogsum is used.
Link to course information is available [here.](https://www.coursera.org/learn/generative-ai-with-llms/home/info)


**Note: The notebooks are supposed to be executed in AWS Sagemaker environment only and are up-to-date as of May 2024. Please do not rerun the notebooks in your own machine.**

## Core libraries used
- datasets
- torch
- torch data
- transformers
- loralib
- evaluate
- rouge_score
- peft
- trl (transformer reinforced-learning)


## Jupyter notebook information
- Lab 1: Generative AI Use Case: Summarize Dialogue
  -  Prompting with Zero/One-shot/Multi-shot Inference with Prompt template
  -  Hyperparameter tuning for Inference involving:
    -   max_new_tokens,
    -   temperature (adjust softmax output probabilities to force randomness or determinism),
    -   do_sample,
    -   top_k (restricts the selection of tokens to the “k” most likely options, based on their probabilities),
    -   top_p(most likely tokens from a probability distribution, considering the cumulative probability until it reaches a predefined threshold “p”.)
- Lab 2: Fine-tune a generative AI model for dialogue summarization
  - Zero Shot inference
  - Full Fine-tuning with preprocessed dialog-summary (prompt-response pair) dataset
  - PEFT tuning with LoRA via PEFT Adapter
  - Evaluation of Model with Human and ROUGE metric (automatic summarization evaluation metric) on full fine-tuning and PEFT.
- Lab 3: Fine-tune FLAN-T5 with reinforcement learning to generate more-positive summaries
  - Using LoRA configurations to train PEFT Adapter added to FLAN-T5
  - Fine tune LLM via Reinforcement Learning (RL) using Proximal Policy Optimization (PPO) model with Meta AI's RoBERTa-based hate speech model acting as reward model (feedback to FLAN-T5 generated summaries)to achieve detoxified summaries, aided by the use of HuggingFace's pipeline library.
