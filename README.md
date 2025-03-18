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

### 31st January

[Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)

- pretrained langauge models store factual information in their weights, hard to pin point 
- retrieval-augmented generation (RAG) model -> retrieve relevant information from a knowledge source and then generate a response
- maginalise latent documents - top-k retrieval - per output basis/token
- retriver (p_n(z|x)) -> x is query and z is the retrived document (BERT Based)
- generator (p(y_i|x,z,y_1:i-1)) -> x is query, z is the retrived document, and y is the output

## 18th March

[Transformers without Normalization](https://arxiv.org/abs/2503.10622)

- DyT: A simple, element-wise operation DyT(x) = tanh(αx) replacing normalization layers in Transformers.
- Inspired by Layer Norm’s S-shaped tanh-like mappings.
- Matches or exceeds performance of normalized Transformers without requiring hyperparameter tuning.
- DyT significantly reduces inference and training time compared to RMSNorm in LLaMA models.