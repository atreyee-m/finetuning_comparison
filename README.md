# Compare various finetuning techniques

## Full Finetuning
- In full fine-tuning, all model parameters (including those in the pre-trained layers and the task-specific layers, such as classification heads) are updated during training.
- The optimizer updates weights of both the pre-trained layers (e.g., BERT encoder) and the new task-specific layers (e.g., classification head).
- It’s computationally more expensive but often achieves higher performance since the entire model is tailored to the new task.

## LoRA (Low-Rank Adaptation)
- LoRA is a fine-tuning technique designed for efficiency, keeping the original model weights frozen while introducing lightweight, trainable adapter layers.
- Instead of modifying all parameters, LoRA applies low-rank decomposition to targeted layers, usually attention mechanisms in transformers.
- It significantly reduces memory usage, training only 1-3% of the parameters, leading to faster and more cost-effective fine-tuning.
- LoRA delivers performance comparable to full fine-tuning while being computationally light, making it ideal for devices with limited resources, such as Apple M3 chips and edge AI applications.
