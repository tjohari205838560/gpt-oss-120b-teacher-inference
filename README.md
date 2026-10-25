This project demonstrates a teacher–student knowledge distillation data-generation pipeline using GPT-OSS-120B on AWS Graviton (ARM64). It uses llama.cpp for CPU-based batch inference on sample FAQs, generating structured question–answer datasets in JSONL format. The pipeline supports resumable inference, response validation, and dataset storage in Amazon S3 for subsequent fine-tuning of a smaller GPT-OSS-20B student model. 

This repository covers the teacher inference and dataset preparation stages only.
