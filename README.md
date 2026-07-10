# 🤖 Automatic Prompt Engineer

> Interactive Prompt Builder for optimizing Large Language Model interactions with automated suggestion and refinement.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)

## 📌 Overview

This project provides an **interactive prompt engineering tool** that helps users:
- Create and refine prompts for LLMs
- Test prompts against different models
- Get suggestions for improvement
- Store and manage prompt libraries
- Analyze prompt performance metrics

## ✨ Features

✅ **Interactive UI** - Build prompts step-by-step  
✅ **Multi-Model Support** - Test with OpenAI, Claude, Gemini  
✅ **Prompt Analysis** - Get metrics on prompt quality  
✅ **Template Library** - Pre-built prompt templates  
✅ **A/B Testing** - Compare prompt variations  
✅ **History Tracking** - Save and manage prompt iterations  

## 🎯 Key Capabilities

### 1. Interactive Prompt Builder
```python
from prompt_engineer import PromptBuilder

builder = PromptBuilder()

# Add components
builder.set_role("expert software engineer")
builder.set_task("write Python code")
builder.set_constraints("no external libraries")
builder.add_examples([
    {"input": "fibonacci", "output": "def fib(n)..."}
])

prompt = builder.generate()
print(prompt)
```

### 2. Prompt Optimization
```python
from prompt_engineer import PromptOptimizer

optimizer = PromptOptimizer()

# Analyze and improve prompt
original = "Write code for sorting"
suggestions = optimizer.analyze(original)

for suggestion in suggestions:
    print(f"- {suggestion.type}: {suggestion.recommendation}")
```

### 3. Multi-Model Testing
```python
from prompt_engineer import MultiModelTester

tester = MultiModelTester()
tester.add_model("gpt-4", api_key=...)
tester.add_model("claude-2", api_key=...)

results = tester.test_prompt(prompt, num_samples=5)
for model, scores in results.items():
    print(f"{model}: {scores['average_quality']:.2f}")
```

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/Baaabaei/Automatic-Prompt-Engineer.git
cd Automatic-Prompt-Engineer

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Basic Usage

```python
from prompt_engineer import PromptBuilder, PromptTester

# Build a prompt
builder = PromptBuilder()
builder.set_role("data scientist")
builder.set_task("analyze sentiment")
prompt = builder.generate()

# Test the prompt
tester = PromptTester(api_key="your-openai-key")
results = tester.test(prompt, test_cases=[
    "This product is amazing!",
    "Not worth the price"
])

print(f"Success rate: {results['success_rate']:.1%}")
```

## 📊 Features Breakdown

### Prompt Components

```yaml
Prompt Structure:
├── Role/Context
│   └── Define who the AI should act as
├── Task Description
│   └── What the AI should do
├── Constraints
│   └── Limitations and requirements
├── Examples (Few-shot)
│   └── Input-output demonstrations
├── Format Instructions
│   └── How to structure responses
└── Tone/Style
    └── Communication style preferences
```

### Analysis Metrics

| Metric | Description |
|--------|-------------|
| Clarity | How clear is the prompt? |
| Specificity | How specific are the instructions? |
| Completeness | Does it cover all requirements? |
| Ambiguity | Are there ambiguous terms? |
| Length | Is it concise? |
| Effectiveness | How well does it perform? |

## 💻 Usage Examples

### Example 1: Building a Customer Service Prompt

```python
from prompt_engineer import PromptBuilder

builder = PromptBuilder()
builder.set_role("customer service representative")
builder.set_task("help customers with product issues")
builder.add_constraint("be empathetic and helpful")
builder.add_constraint("respond within 2 sentences")
builder.add_example(
    input_text="Product stopped working",
    output_text="I'm sorry to hear that! Let's troubleshoot...."
)

prompt = builder.generate()
```

### Example 2: Comparing Prompt Variations

```python
from prompt_engineer import MultiModelTester

prompts = {
    "basic": "Write a poem about nature",
    "detailed": "Write a 10-line poem about nature in spring with imagery",
    "constrained": "Write a poem about nature (10 lines, spring theme, no rhyming)"
}

tester = MultiModelTester()
for name, prompt in prompts.items():
    score = tester.evaluate(prompt)
    print(f"{name}: {score.effectiveness:.2f}")
```

### Example 3: A/B Testing

```python
from prompt_engineer import ABTester

tester = ABTester()

prompt_a = "Summarize this text"
prompt_b = "Provide a concise 2-3 sentence summary of this text"

results = tester.compare(prompt_a, prompt_b, iterations=100)
print(f"Winner: {results['winner']}")
print(f"Improvement: {results['improvement']:.1%}")
```

## 🏗️ Architecture

```
┌──────────────────────────────────┐
│   Interactive UI (Streamlit)     │
└────────────────┬─────────────────┘
                 │
    ┌────────────┼────────────┐
    │            │            │
    ▼            ▼            ▼
┌──────────┐ ┌──────────┐ ┌──────────┐
│ Builder  │ │ Analyzer │ │ Tester   │
└────┬─────┘ └────┬─────┘ └────┬─────┘
     │            │            │
     └────────────┼────────────┘
                  ▼
         ┌─────────────────┐
         │  Prompt Storage │
         │   & History     │
         └─────────────────┘
                  │
     ┌────────────┼────────────┐
     │            │            │
     ▼            ▼            ▼
  OpenAI       Claude       Gemini
   API          API          API
```

## 🧪 Testing

```bash
# Run tests
python -m pytest tests/

# Test with coverage
python -m pytest --cov=prompt_engineer tests/
```

## 📚 Template Library

Pre-built templates for:
- Code generation
- Text summarization
- Sentiment analysis
- Question answering
- Creative writing
- Data analysis

## 🤝 Contributing

Contributions welcome! Areas:
- New templates
- Additional models
- Analysis metrics
- UI improvements

## 📄 License

MIT License - See [LICENSE](LICENSE) file.

## 🗺️ Roadmap

- [ ] Web-based UI
- [ ] More model integrations
- [ ] Prompt marketplace
- [ ] Team collaboration features
- [ ] Advanced analytics dashboard

## ⭐ Show Your Support

If this tool helps with prompt engineering:
- ⭐ Star this repository
- 🔗 Share with your team
- 💬 Leave feedback
- 🤝 Contribute templates/improvements

---

**Optimizing Prompt Engineering! 🚀**

*Last Updated: July 2026 | Maintained by [@Baaabaei](https://github.com/Baaabaei)*
