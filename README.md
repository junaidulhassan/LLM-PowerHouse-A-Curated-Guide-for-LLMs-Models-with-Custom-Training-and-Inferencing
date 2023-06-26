# Custom-Large-Language-Model
Allows for domain-specific knowledge, customized responses, enhanced creativity, improved conversational abilities, data privacy, local deployment, and research opportunities. It offers tailored and specialized AI applications by fine-tuning the model to specific preferences, guidelines, and subject matter expertise.

# Prompt Engineering

Prompt engineering is a technique that can be used to improve the performance of LLMs on specific tasks. It involves crafting prompts that help the LLM to generate the desired output. This can be done by providing the model with additional information, such as examples of the desired output, or using specific language the model is likely to understand. 

Prompt Engineering can be powerful tool, but it is important to note that it is not a silver bullet. LLMs can still generate incorrect or unexpected output even with the best prompts. As a result, it is important to test the output of LLMs carefully before using them in production. 

# Fine Tuning
In other hand, fine-tuing is adapting a pre-trained LLM to a specific task or domain by training it further on a smaller, task-specific dataset. This is done by adjusting the model's weights and parameters to minimize the loss function and improve its performance on the task.

Fine-tuning can be more effective way to improve the performance of LLMs on specific tasks that prompt engineering. However, it is also more time-consuming and expensive. As a result, it is important to consider the cost and time involved in fine-tuning before deciding whether to use it. 

# When to perform

Fine-tuning is typically needed when the task is new or challenging or when the desired output is highly specific. In these cases, prompt engineering may not be able to provide the model with enough information to generate the desired output. 

Prompt engineering is typically sufficient when the task is well-defined and the desired output could be more specific. In these cases, prompt engineering can provide the model with the information it needs to generate the desired output. 


# What I am learning

After immersing myself in the recent GenAI text-based language model hype for nearly a month, I have made several observations about its performance on my specific tasks.

Please note that these observations are subjective and specific to my own experiences, and your conclusions may differ.

- We need a minimum of 7B parameter models (<7B) for optimal natural language understanding performance. Models with fewer parameters result in a significant decrease in performance. However, using models with more than 7 billion parameters requires a GPU with greater than 24GB VRAM (>24GB).
- Benchmarks can be tricky as different LLMs perform better or worse depending on the task. It is crucial to find the model that works best for your specific use case. In my experience, MPT-7B is still the superior choice compared to Falcon-7B.
- Prompts change with each model iteration. Therefore, multiple reworks are necessary to adapt to these changes. While there are potential solutions, their effectiveness is still being evaluated.
- For fine-tuning, you need at least one GPU with greater than 24GB VRAM (>24GB). A GPU with 32GB or 40GB VRAM is recommended.
- Fine-tuning only the last few layers to speed up LLM training/finetuning may not yield satisfactory results. I have tried this approach, but it didn't work well.
- Loading 8-bit or 4-bit models can save VRAM. For a 7B model, instead of requiring 16GB, it takes approximately 10GB or less than 6GB, respectively. However, this reduction in VRAM usage comes at the cost of significantly decreased inference speed. It may also result in lower performance in text understanding tasks.
- Those who are exploring LLM applications for their companies should be aware of licensing considerations. Training a model with another model as a reference and requiring original weights is not advisable for commercial settings.
- There are three major types of LLMs: basic (like GPT-2/3), chat-enabled, and instruction-enabled. Most of the time, basic models are not usable as they are and require fine-tuning. Chat versions tend to be the best, but they are often not open-source.
- Not every problem needs to be solved with LLMs. Avoid forcing a solution around LLMs. Similar to the situation with deep reinforcement learning in the past, it is important to find the most appropriate approach.
- I have tried but didn't use langchains and vector-dbs. I never needed them. Simple Python, embeddings, and efficient dot product operations worked well for me.
- LLMs do not need to have complete world knowledge. Humans also don't possess comprehensive knowledge but can adapt. LLMs only need to know how to utilize the available knowledge. It might be possible to create smaller models by separating the knowledge component.
- The next wave of innovation might involve simulating "thoughts" before answering, rather than simply predicting one word after another. This approach could lead to significant advancements.
