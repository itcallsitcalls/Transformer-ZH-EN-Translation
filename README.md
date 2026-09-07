# Transformer‑ZH‑EN‑Translation
> PyTorch从零复现标准Transformer Encoder‑Decoder架构，实现WMT2018英→中机器翻译任务。
> 完整实现词嵌入、位置编码、多头注意力、残差+LayerNorm、Encoder/Decoder层、Beam Search解码。

## 项目简介
基于WMT2018新闻翻译中英双语数据集（252777平行句对），从零实现原生Transformer机器翻译模型。
1. 数据处理：json原始数据抽取、语料统计、sentencepiece子词分词器训练；
2. 模型实现：完整Encoder‑Decoder，多头注意力、掩码注意力、位置编码、残差层归一化；
3. 训练策略：Noam学习率调度；
4. 评估指标：**BLEU=26.38**；支持Beam‑Search解码，交互式英文翻译推理。

### 实验指标
- 数据集：WMT2018新闻翻译，252777中英平行句对
- 最优验证BLEU：**26.38**
- 训练硬件：RTX4060显卡，batch_size=32

## 环境依赖
```bash
pip install -r requirements.txt
