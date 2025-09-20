# README

## Introduction
This project demonstrates **Direct Preference Optimization (DPO)** using the Hugging Face `trl` library.  
DPO is a method designed to directly optimize **large language models (LLMs)** based on **human preference data**, improving their alignment with user expectations without requiring reinforcement learning from scratch.

Unlike traditional methods such as **Proximal Policy Optimization (PPO)**, DPO simplifies the training pipeline by directly optimizing the likelihood ratio between preferred and non-preferred responses.  

By completing this lab, you gain hands-on experience in:
- Formatting datasets for DPO.  
- Implementing optimization with Hugging Face’s `trl` library.  
- Fine-tuning LLMs for preference alignment.  
- Evaluating improvements before and after DPO training.  

---

## Implementation
1. **Setup**  
   - Installed required dependencies (`transformers`, `trl`, `datasets`, `bitsandbytes` for optional quantization).  
   - Imported libraries for model loading, training, and evaluation.  

2. **Model and Tokenizer Configuration**  
   - Loaded a pretrained language model from Hugging Face Hub.  
   - Configured the tokenizer to handle text preprocessing.  
   - (Optional) Used **quantized model configuration** with `bitsandbytes` for memory-efficient training.  

3. **Dataset Preparation**  
   - Created a dataset including **pairs of responses**: one preferred by humans, one not preferred.  
   - Preprocessed the dataset into the format required by the `trl` library for DPO training.  

4. **DPO Configuration**  
   - Defined training arguments such as learning rate, batch size, and optimization steps.  
   - Configured the **DPO trainer** with the model, tokenizer, and dataset.  

5. **Training with DPO**  
   - Ran fine-tuning using the DPO trainer.  
   - Trained either the **full model** or a **LoRA-adapted version** for efficiency.  

6. **Evaluation**  
   - Compared model responses **before and after DPO fine-tuning**.  
   - Evaluated alignment improvements by checking whether the model better matched human-preferred outputs.  

---

## Conclusion
This lab highlights the effectiveness of **Direct Preference Optimization (DPO)** for aligning large language models with human expectations.  

Key takeaways:  
- DPO simplifies preference optimization compared to reinforcement learning–based methods like PPO.  
- Human preference data, when formatted properly, can significantly improve LLM outputs.  
- LoRA and quantized models allow efficient fine-tuning without requiring massive GPU resources.  
- The trained model demonstrates measurable improvements in **alignment with user-preferred responses**.  

This makes DPO a practical and scalable method for fine-tuning LLMs in real-world applications where **user alignment** is critical.  
