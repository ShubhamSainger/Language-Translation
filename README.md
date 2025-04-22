
# Neural Machine Translation with Attention Mechanism

This repository contains a PyTorch implementation of the research paper [**"Neural Machine Translation by Jointly Learning to Align and Translate"**](https://arxiv.org/abs/1409.0473) by Bahdanau et al. (2015). This paper introduced the **attention mechanism**, a key innovation that later influenced the development of the Transformer architecture.

## 🧠 Paper Summary

The paper proposes an encoder-decoder architecture with an attention mechanism that allows the model to focus on different parts of the input sequence while generating each word of the output sequence. This approach overcomes the bottleneck of encoding the entire source sentence into a single fixed-size context vector.

> *“Instead of encoding a full sentence into a fixed-length vector, the model learns to align and translate jointly by attending to relevant parts of the source sentence during decoding.”*

---

## ✨ Key Features

- Encoder-decoder architecture using LSTM (Long Short Term Memory)
- Additive attention mechanism (Bahdanau Attention)
- Trained on parallel corpora (e.g., English-Hindi)
- Implemented from scratch using **PyTorch**

---

## Dataset

- Source : English-Hindi sentences pair from [Tatoeba](https://tatoeba.org/en) 
- Size :  12000 pairs of sentences
  
## 🛠️ Model Architecture

- **Encoder**: Bi-directional LSTM network that processes the source sentence and returns the state for each token in the sequence
- **Decoder**: A network that generates the target sentence by taking the hidden states returned by the encoder, it's own previous state and the last predicted token
- **Attention Mechanism**: Computes alignment scores between encoder hidden states and decoder hidden state at each time step
- **Max Out Layer**: Created a customized Max Out layer which will project the activations from the LSTM layer of decoder into two different vector spaces and choose the maximum value of the element from both the projections and then used to compute the softmax probabilities
- **Byte-Pair Tokenizer**: The tokenizer was trained using Hugging Face's BPE model to iteratively merge the most frequent pairs of characters or subwords from the corpus, effectively building a vocabulary of size 10000 based on the English and Hindi corpus.
- **Custom Training Loop**: The custom loop allows fine-grained control over training, enabling dynamic adjustments to hyperparameters, batch sizes, and evaluation intervals.

## 📜 Citation
- Dzmitry Bahdanau, Kyunghyun Cho, Yoshua Bengio.
[_Neural Machine Translation by Jointly Learning to Align and Translate, ICLR 2015_.](https://arxiv.org/abs/1409.0473)


## 🤝 Contributions

Feel free to contribute! Open an issue or create a pull request if you'd like to improve the project. 🚀

## 📧 Contact

For any queries, reach out via:

- 🔗 LinkedIn: [Shubham Singh Sainger](https://www.linkedin.com/in/shubham-sainger/)
- 📧 Email: [shubhamsainger97@gmail.com](mailto\:shubhamsainger97@gmail.com)
---
