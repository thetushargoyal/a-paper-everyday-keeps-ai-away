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

### 30th January

[AN IMAGE IS WORTH 16X16 WORDS: TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE](https://arxiv.org/abs/2010.11929)

- Transformer take less training resources than a CNN
- Before this paper, people tried to use Transformers but couldn't scale because they didn't leverage modern GPU architecture for acceleration
- Transformers lack inductive bias (built-in assumption a model has about the data) inherent to CNNs, such as translation equivariance and locality
- Vision Transformer (ViT) -> split image into patches, flatten them, add positional embeddings, and feed them to a Transformer