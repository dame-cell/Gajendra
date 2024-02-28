# Gaja

We release Gaja , a Hindi/Hinglish chat model instruction finetuned on SarvamAI's OpenHathi model.

<p align="center">
  <img src="asset\Dariava.jpg" alt="Gajendra is a Hindi/Hinglish instruction-tuned model based on different instruct datasets." style="width: 45%; min-width: 300px;">
</p>


This repository contains the code for  "Gaja", a project focused on Fine-Tuning SarvamAI's OpenHathi model for Conversational task . which employs the LoRA + Unsloth methodology for efficient fine tuning. 

# Contents 
1) [Indic-Eval](#indic-eval)
2) [Usage-Note](#usage-note)
3) [Prompt](#prompt)

If you appreciate this work and found it helpful, consider giving it a star ⭐️ on GitHub. Your support motivates me to continue improving and adding new features. Thank you for your encouragement!

# Indic-Eval
Performing zero-shot Evaluation on the model : 

| Task                   | # Samples | Accuracy | Precision | F1       | Recall   |   Metrics  | 
|------------------------|-----------|----------|-----------|----------|----------|------------|
| Indic-Sentiment Analysis     |    100   |  0.71    |   -       | 0.76     | -    |   Accuracy,F1 score          |
| Indic-QA Evaluation    |    50    | -    |   0.62      |  0.68    | 0.75   |       Bert Score          |
| Indic-Summarization Evaluation |  50    |  -       |   0.65      | 0.68     |0.72   |   Bert Score          |
| Indic-NLI                       | 50     | 0.24    |   -       | 0.17       |        |     Accuracy,F1 score              |

# Prompt 

The prompt for the Model without system prompt 
```python
<|im_start|>user
{}<|im_end|> 
<|im_start|>assistant
{}<|im_end|> 
```
The prompt for the Model with system prompt 
```python
|im_start|>system
{}<|im_end|> 
<|im_start|>user
{}<|im_end|> 
<|im_start|>assistant
{}<|im_end|> 
```

# Usage-Note
It's important to note that the models have not undergone detoxification. Therefore, while they possess impressive linguistic capabilities, there is a possibility for them to generate content that could be deemed harmful or offensive. We urge users to exercise discretion and supervise the model's outputs closely, especially in public or sensitive applications.
