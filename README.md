## Project Title: AD 331 Fine-Tuning a Pre-trained LLM (PEFT/LoRA)
#### By: Amde Wubshet

### LoRA Configuration Parameters:
- r=8,  
- lora_alpha=16,
- target_modules=["query", "value"],
- lora_dropout=0.1, 
- bias="none", 
- task_type=TaskType.SEQ_CLS 

### Final Evaluation Metrics 
- Accuracy: 0.91552
- F1:  0.9168634860651866
- precision: 0.902510849349039 
- recall: 0.93168

### Why does LoRA save computational resources? 
- LoRA saves computational resources by freezing most of the large pre-trained model's weights and introducing small, trainable "adapter" matrices (low-rank matrices) to specific layers, drastically reducing the number of parameters that need updating. This minimizes memory (VRAM) usage, speeds up training, lowers GPU hours, and allows fine-tuning large models on consumer-grade hardware, making AI more accessible