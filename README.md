## An Optimized Large Language Model for Korean Colloquial Language

This repository contains the codebase for EXASPO, a Korean colloquial-specific LLM designed to enhance natural and engaging Korean conversation.   
EXASPO is built upon the Korean-dominant EXAONE-3.5 models (2.4B and 7.8B) and is continually pre-trained on 9.5 GB of Korean colloquial data, followed by instruction tuning to generate contextually appropriate colloquial responses.

You can find our model on the HuggingFace Hub: https://huggingface.co/JunHaHwang/EXASPO-3.5-7.8B-Instruct

### Environment Setup

It is recommended to use a virtual environment (e.g. `venv`). 

Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### How to Run

1. **Model Training**:
   * For Continual Pre-Training: Run `notebooks/Continual_PreTraining.ipynb`
   * For Instruction Tuning: Run `notebooks/Instruction_Tuning.ipynb`

2. **Benchmarking Inference**:
   After training, run `notebooks/Benchmark_Inference_EXAONE.ipynb` or `notebooks/Benchmark_Inference_EXASPO.ipynb` to generate and evaluate responses.


### Code Overview

* **Continual Pre-Training**:
  * `notebooks/Continual_PreTraining.ipynb`: Continual pre-training code for the EXAONE 3.5 model.
* **Instruction Tuning**:
  * `notebooks/Instruction_Tuning.ipynb`: Instruction tuning code using SFTTrainer.
* **Data Packing and Preprocessing**: 
  * `notebooks/Benchmark_Preprocessing.ipynb`: Custom preprocessing logic for the benchmark dataset.
  * `notebooks/Packing_Data.ipynb`: Data parsing and packing for efficient training.
* **Benchmarking & Inference**: 
  * `notebooks/Benchmark_Inference_EXAONE.ipynb` \& `notebooks/Benchmark_Inference_EXASPO.ipynb`: Benchmark Inference wih LLM Judge (GPT-4o-mini).
