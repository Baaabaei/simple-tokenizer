# Simple Tokenizer

A lightweight, educational tokenizer built from scratch for encoding and decoding simple English text, designed for understanding the fundamentals of tokenization in Large Language Models (LLMs).

---

## 📖 About

This repository contains a simple, educational tokenizer that demonstrates the core concepts behind how LLMs process text. It's built entirely in Python without external dependencies, making it perfect for learning how tokenization works under the hood.

**Created by:** [Baaabaei](https://github.com/Baaabaei)

---

## ✨ Features

- **Basic Text Encoding**: Convert text into token IDs
- **Text Decoding**: Convert token IDs back to readable text
- **Simple Vocabulary**: Understand the mapping between tokens and IDs
- **Educational Focus**: Clean, readable code for learning purposes
- **No External Dependencies**: Pure Python implementation

---

## 📁 Repository Structure

```
simple-tokenizer/
├── simple_tokenizer.py      # Version 1: Basic implementation
├── simple_tokenizer_v2.py   # Version 2: Improved/enhanced version
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- No additional libraries required

### Installation

```bash
# Clone the repository
git clone https://github.com/Baaabaei/simple-tokenizer.git

# Navigate to the project directory
cd simple-tokenizer

# Run the tokenizer
python simple_tokenizer.py
```

---

## 💻 Usage Examples

### Basic Tokenization

```python
from simple_tokenizer import SimpleTokenizer

# Initialize the tokenizer
tokenizer = SimpleTokenizer()

# Example text
text = "Hello, world! This is a simple tokenizer."

# Encode text to token IDs
tokens = tokenizer.encode(text)
print(f"Tokens: {tokens}")

# Decode token IDs back to text
decoded_text = tokenizer.decode(tokens)
print(f"Decoded: {decoded_text}")
```

---

## 🔧 Implementation Details

### How It Works

1. **Vocabulary Building**: Creates a mapping between words/subwords and unique IDs
2. **Encoding Process**: Splits text into tokens and converts to IDs
3. **Decoding Process**: Converts token IDs back to readable text

### Key Components

- **Tokenizer Class**: Main class handling encode/decode operations
- **Vocabulary**: Dictionary mapping tokens to integer IDs
- **Special Tokens**: Handles unknown/out-of-vocabulary tokens

---

## 📊 Comparison: Simple Tokenizer vs. Advanced Tokenizers

| Feature | Simple Tokenizer | BPE Tokenizer | SentencePiece |
|---------|-----------------|---------------|---------------|
| **Complexity** | Simple | Moderate | Advanced |
| **Subword Support** | ❌ No | ✅ Yes | ✅ Yes |
| **Unknown Token Handling** | Basic | Advanced | Advanced |
| **Educational Value** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ |
| **Use Case** | Learning | Production | Production |

---

## 🎯 Purpose & Learning Goals

This project is designed to help developers understand:
- **Fundamental Concepts**: How tokenization forms the first step in NLP pipelines
- **Inner Workings**: What happens when text is converted to numbers for model processing
- **Implementation Basics**: How to build a simple but functional tokenizer
- **LLM Foundation**: Why tokenization is crucial for language models

---

## 🛠️ Future Improvements

Potential enhancements that could be added:
- [ ] Subword tokenization (BPE/WordPiece)
- [ ] Support for non-English text
- [ ] Special token handling ([UNK], [PAD], [CLS])
- [ ] Vocabulary size configurability
- [ ] Save/load vocabulary functionality
- [ ] Performance optimizations
- [ ] Unit tests
- [ ] Command-line interface

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request
4. Open issues for bugs or suggestions

---

## 📚 Learning Resources

For those wanting to dive deeper into tokenization:
- **Hugging Face Tokenizers**: Production-ready tokenization library
- **GPT-2 Tokenizer**: BPE implementation by OpenAI
- **SentencePiece**: Google's subword tokenizer
- **BERT Tokenizer**: WordPiece implementation

---

## 📄 License

This project is open source and available under the MIT License.

---

## 👤 Author

**Baaabaei**
- GitHub: [@Baaabaei](https://github.com/Baaabaei)

---

## ⭐ Support the Project

If you find this project helpful for learning:
- Star the repository ⭐
- Share with others learning about LLMs
- Contribute improvements
- Open issues for questions

---

## 🧠 Why Tokenization Matters

Tokenization is the critical first step in all modern NLP/LLM pipelines:

```
1. Input Text → 2. Tokenization → 3. Token IDs → 4. Embeddings → 5. Model Processing
```

Understanding tokenization helps demystify how models like GPT, BERT, and other LLMs process text data.

---

## 📞 Contact & Support

For questions or support:
- Open an issue on GitHub
- Reach out to the maintainer
- Check the documentation

---

*Built with ❤️ for the developer community*
