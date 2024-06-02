# Mental Health Chatbot Project

blog link - https://sumedhapandravada.wixsite.com/therapease/post/pandora

## Overview

The Mental Health Chatbot project aims to foster well-being by offering empathetic interactions tailored to users' mental health needs. This chatbot is built by fine-tuning the MentaLLaMA-chat-7B model using a custom dataset to enhance its ability to provide mental health support and information.

## Functionality

The chatbot is designed to:
- Answer questions related to mental health.
- Provide support and information on various mental health conditions.
- Offer reliable explanations and empathetic responses to users.
  

## About MentaLLaMA

MentaLLaMA-chat-7B is part of the MentaLLaMA project, the first open-source large language model (LLM) series for interpretable mental health analysis with instruction-following capability. It is fine-tuned based on the Meta LLaMA2-chat-7B foundation model and the full IMHI instruction tuning data.


## Incorporating the Dataset for Fine-tuning

### Dataset Description

The dataset can be accessed [here](https://huggingface.co/datasets/AnanyaA/Therapease). It consists of diverse mental health-related conversations. It includes:
- **Questions** asked by users.
- **Responses** provided by the chatbot.

### Fine-tuning Process

We fine-tuned the MentaLLaMA-chat-7B model using the QLoRA (Quantized Low-Rank Adaptation) technique. This method updates only 1 to 10% of the parameters, making the process more efficient. To drastically reduce the VRAM usage, we must fine-tune the model in 4-bit precision, which is why we’ll use QLoRA here. The fine-tuning steps are as follows:
1. **Model Selection**: We used the `klyang/MentaLLaMA-chat-7B` model as the base.
2. **Dataset Loading**: Our custom dataset was loaded and pre-processed.
3. **QLoRA Configuration**: Specific parameters for LoRA and BitsAndBytes configurations were set.
4. **Training**: The model was trained with specific training arguments tailored for our dataset.
5. **Evaluation and Testing**: Post-training, the model was evaluated for its performance on mental health-related queries.

### Technical Requirements

- **Supercomputer Access**: Due to the model's size and complexity, fine-tuning requires significant computational resources. Access to a supercomputer or a high-end GPU cluster is recommended.
- **Hugging Face Integration**: The model and dataset are integrated with the Hugging Face ecosystem for ease of use and deployment.
- **for that chat**: Text generation pipeline to ask questions and receive responses from the chatbot.


