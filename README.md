# Compare various finetuning techniques

## Full Finetuning
- In full fine-tuning, all model parameters (including those in the pre-trained layers and the task-specific layers, such as classification heads) are updated during training.
- The optimizer updates weights of both the pre-trained layers (e.g., BERT encoder) and the new task-specific layers (e.g., classification head).
- It’s computationally more expensive but often achieves higher performance since the entire model is tailored to the new task.

