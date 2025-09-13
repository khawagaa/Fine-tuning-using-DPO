# Direct Preference Optimization (DPO) with Hugging Face

This project demonstrates how to apply **Direct Preference Optimization (DPO)** using Hugging Face’s ecosystem.  
DPO is a reinforcement learning–free method for aligning large language models with human preferences.  
Instead of relying on traditional RLHF (Reinforcement Learning with Human Feedback), DPO optimizes models directly with pairwise preference data, making it simpler and more efficient.

---

## 📌 Project Overview

1. **Objective**  
   Fine-tune a pretrained language model using DPO, enabling it to better align with human preferences without the complexity of reinforcement learning.

2. **Dataset**  
   - Uses preference-labeled data (pairs of "chosen" vs "rejected" responses).  
   - Demonstrates how to format, preprocess, and integrate such data with Hugging Face’s training pipeline.  

3. **Method**  
   - Start with a base model from Hugging Face Hub.  
   - Apply Direct Preference Optimization (DPO).  
   - Evaluate improvements in model alignment.  

---

## ⚙️ Installation

Make sure you have Python 3.8+ installed. Then install dependencies:

```bash
pip install torch transformers datasets accelerate peft trl
📂 Files in This Repo
Lab_Direct_Preference_Optimization_(DPO)_using_Hugging_Face_solution.ipynb
Jupyter notebook with the full workflow: dataset loading, preprocessing, DPO training, and evaluation.

README.md
You’re reading it. Provides documentation for setup and usage.

🚀 Usage
Clone the repository:

bash
Copy code
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
Open the notebook:

bash
Copy code
jupyter notebook Lab_Direct_Preference_Optimization_(DPO)_using_Hugging_Face_solution.ipynb
Run cells step by step to:

Load dataset

Format preference pairs

Fine-tune with DPO

Evaluate results

📊 Expected Results
The model should demonstrate improved alignment with human-preferred outputs compared to baseline.

Performance can be measured by evaluating generated outputs or via preference accuracy on a held-out test set.

🔮 Future Work
Experiment with different base models from Hugging Face Hub.

Scale to larger preference datasets for stronger alignment.

Compare DPO with RLHF approaches.

📜 References
Hugging Face TRL library: https://huggingface.co/docs/trl

Original DPO paper: Direct Preference Optimization: Your Language Model is Secretly a Reward Model

