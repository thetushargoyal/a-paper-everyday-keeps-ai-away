### 26th January

[DeepSeek R1](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf)

- a little Supervised Fine-Tuning data, with a good reinforcement learning model, can go a long way in improving the performance of a model.
- again never accept the status quo of the industry -> Nvidia 15% down :P

### 29th January

[LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)

- freeze pretrained weights and inject low-rank matrices (same size when multiplied to full rank matrics) to adapt to new tasks
- no additional inference latency, combine with weight matrix -> W = W_0 + BA
- insight -> model adaptation is a low-rank problem
- over parameterizatised models have meaning in low intrinsic dimension
