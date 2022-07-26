---
title: transformer
date: 2022-07-26
author: Hannah Jaywon Kim
description: Transformer summary
---
# Transformer
## Attension is all you need

Transformer is a model which follows the structure of the previous seq2seq model, only using Attension. This RNN-removed encoder-decoder structure was suggested in 2017, presented by Google. The paper showed that this model acheived better performance at translating than RNN.

Below is the contents of this post.
1. Limitations of seq2seq model
2. Structure of Transformer
3. reference

## 1. Limitations of seq2seq model
When the incoder RNN returns the context vector in encoder-decoder structure, some information of the original input sequence get lost. This is the reason why seq2seq model used attension to suplement RNN and achieve a better performance at remembering previous inputs. So why only use attension as a supplement of RNN, but as encoders and decoders itself?
## 2. Structure of Transformer

## 3. Reference
딥 러닝을 이용한 자연어 처리 입문 (2022) 유원준 외. ([https://wikidocs.net/31379](https://wikidocs.net/31379))
