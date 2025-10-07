# Gen-AI-with-LLMs---Fine-Tune-a-Generative-AI-Model-for-Dialogue-Summarization
# Fine-Tuning FLAN-T5 for Dialogue Summarization 🚀

This notebook provides a hands-on guide to **fine-tuning** an existing Large Language Model (LLM) from Hugging Face for enhanced dialogue summarization. You'll start with the powerful **FLAN-T5** model, a high-quality, instruction-tuned model that can summarize text out of the box.

To improve its inferences on a specific dataset, you will explore and compare two core approaches: a **full fine-tuning** approach and **Parameter Efficient Fine-Tuning (PEFT)**. You will evaluate the results of both methods using **ROUGE metrics** to see firsthand how the benefits of PEFT (like reduced computational cost) often outweigh a slight difference in performance.

---

## 🎯 Objectives

By completing this notebook, you will:

* **Implement** a full fine-tuning pipeline for the FLAN-T5 model.
* **Perform** Parameter Efficient Fine-Tuning (PEFT) on the same model.
* **Evaluate** the performance of both resulting models using the ROUGE metric.
* **Compare** the trade-offs between full fine-tuning and PEFT in terms of performance and resource efficiency.

---

## 🛠️ Key Concepts

### FLAN-T5
**FLAN-T5** is an instruction-tuned language model based on the T5 architecture. It has been trained to follow a wide variety of instructions, making it a strong baseline model for tasks like summarization even before fine-tuning.

### Full Fine-Tuning
This is the traditional approach where **all the weights** of the pre-trained model are updated during training on a new, task-specific dataset. While it can achieve high performance, it is computationally intensive, requiring significant memory and time.

### Parameter Efficient Fine-Tuning (PEFT)
PEFT is a collection of techniques designed to adapt large models to new tasks by training only a **small fraction** of their parameters. This makes fine-tuning much more accessible, drastically reducing memory requirements and training time without a significant drop in performance.

### ROUGE Metrics
**ROUGE** (Recall-Oriented Understudy for Gisting Evaluation) is a set of metrics used to automatically evaluate text summarization. It works by comparing the n-grams (sequences of words) in the model-generated summary to the n-grams in a human-written reference summary.

---

## 📝 Workflow

1.  **Setup**: Load the pre-trained FLAN-T5 model and tokenizer, along with the dialogue dataset.
2.  **Baseline Inference**: Test the out-of-the-box performance of the base FLAN-T5 model.
3.  **Full Fine-Tuning**: Fine-tune all parameters of the model on the training data.
4.  **PEFT**: Apply a PEFT method (like LoRA) to train only a small number of new parameters.
5.  **Evaluation**: Run inference with both fine-tuned models and evaluate their summaries against reference texts using ROUGE scores.
6.  **Analysis**: Compare the ROUGE scores, training times, and resource usage of each method to conclude when and why PEFT is the superior approach.
