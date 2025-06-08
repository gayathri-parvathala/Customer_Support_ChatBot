# Customer Support Chatbot using TinyLlama (Colab + T4 GPU)

This project implements a lightweight customer support chatbot powered by the open-source [TinyLlama/TinyLlama-1.1B-Chat-v1.0](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0) language model. The application runs entirely in Google Colab using a T4 GPU and is served through a Gradio web interface.

## Features

- **Model:** TinyLlama-1.1B-Chat (causal language model)
- **Inference:** GPU-accelerated using `torch.float16` on Google Colab (T4 GPU)
- **Interface:** Gradio `ChatInterface` with fallback to `Blocks`
- **Knowledge Base:** Static FAQ matching with LLM reasoning
- **Prompting:** Custom prompt building with context and history

## Sample Use Cases

The chatbot can answer customer queries related to:

- Order tracking  
- Return and exchange policy  
- Shipping information  
- Payment options (UPI, Wallets, Cards)  
- Product specifications (smartphones, laptops)  
- Warranty details  
- Customer support contact  
- Order cancellation  

You can easily expand the static FAQ dictionary to support more topics.

## Installation & Execution (Google Colab)

1. **Set Runtime to GPU**

   - `Runtime > Change runtime type > GPU (T4 preferred)`

2. **Install Required Packages**

```python
!pip install transformers gradio accelerate
