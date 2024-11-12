# Generative AI for Creative Problem Solving

**Abstract**

The rapid advances in generative AI have the potential to reshape organizational innovation, raising uncertainty about the role of human solvers in this new era of augmented intelligence. We initiated a crowdsourcing challenge focused on sustainable, circular economy business opportunities, comparing the capabilities of GPT-4 and human solvers in generating novel and valuable solutions. The challenge attracted a diverse range of global solvers from various industries. 300 evaluators assessed a randomized selection of 13 out of 234 human and AI solutions, totaling 3,900 evaluator–solution pairs. Our findings reveal that, although AI solutions delivered more environmental and financial value—possibly due to a tendency to align with the central patterns seen in their training—human outputs were rated as more innovative, including extreme outcomes at the right tail of the novelty distribution. Our analysis of the rich solution text using natural language processing techniques reveals considerable overlap in semantic dissimilarity metrics between human and AI responses, but humans still exhibit greater linguistic nuances than AI. This study illuminates the promise of AI in augmenting human crowdsourcing for solving complex organizational problems and sets the groundwork for a possible integrative human-AI approach to innovative problem-solving.

Keywords: Generative AI, ChatGPT, LLMs, innovation, crowdsourcing, idea generation, evaluation, novelty, value

[Paper link](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4533642)

Authors: 
Leonard Boussioux*, Jacqueline N Lane*, Miaomiao Zhang, Vladimir Jacimovic, Karim R Lakhani
* = equal contribution

The code below generates the problem-solution pairs of the 3 levels, with multiple and single instances.
You can replicate our experiments with this Google colab notebook in Python: [here](https://colab.research.google.com/drive/1tpqQ_hWAbrfaQUUkVEm_EEqtVbuislUg?usp=sharing).

## Key Insights From Code 

The Power of Prompt Engineering: Discover how different prompt engineering strategies influence the quality and relevance of GPT-4's output.
Recent studies hint at the tendency of LLMs, like GPT-4, to produce homogenized outputs, potentially stifling the diversity of creative solutions. To address this, we've devised and tested two innovative configurations of GPT-4 aimed at boosting the variety of generated ideas:

1. **Multiple-Instance Solutions**: This setup leverages separate instances of GPT-4, each tasked with generating a unique solution based on the same prompt. This method takes advantage of the LLM's sampling techniques to ensure a broad spectrum of responses, despite identical inputs.

2. **Single-Instance Solutions with Differentiation Instructions**: Here, a single GPT-4 instance generates multiple, distinct solutions in sequence, guided by instructions to diversify outputs. This approach simulates an iterative brainstorming process, pushing the boundaries of creativity and uniqueness in solution generation.

# Generative AI and Creative Problem Solving

This repository contains the code implementation for the research study "The Crowdless Future? Generative AI and Creative Problem-Solving", which explores the comparative capabilities of GPT-4 and human solvers in generating innovative solutions for sustainable, circular economy business opportunities.

## 🎯 Research Overview

The study examines:
- The effectiveness of GPT-4 vs. human solvers in generating novel and valuable solutions
- Different prompt engineering strategies for generating AI solutions
- The impact of multiple-instance and single-instance configurations on solution diversity
- Natural language processing analysis of solution text semantics

## 📊 Study Design

The experiment involves:
- A crowdsourcing challenge focused on circular economy business opportunities
- 234 total solutions (human and AI-generated)
- 300 evaluators assessing randomized selections
- 3,900 total evaluator-solution pairs

## 🛠️ Technical Implementation

The code is organized into three main levels, each with multiple and single instance configurations:

### Level 1: Base Prompt
- Implementation of basic prompt engineering
- No specific persona assignment
- Available in both multiple (1M) and single (1S) instance versions

### Level 2: Persona-Based
- Incorporates diverse personas into prompt engineering
- Structured approach to persona integration
- Available in both multiple (2M) and single (2S) instance versions

### Level 3: Expert Persona
- Utilizes real-world expert personas from 23 different fields
- 5 experts per field for diverse perspective
- Available in both multiple (3M) and single (3S) instance versions

## 🚀 Getting Started

### Prerequisites
```python
pip install openai
```

### Configuration
1. Set up your OpenAI API key:
```python
client = OpenAI(
    api_key="YOUR_API_KEY"
)
```

2. Adjust the number of responses as needed:
```python
n_answers = 100  # Default setting for full implementation
```

## 📝 Implementation Details

### Data Generation Functions
- `generate_responses_level1M()`: Generates multiple-instance base responses
- `generate_responses_level2M()`: Generates multiple-instance persona-based responses
- `generate_responses_level3M()`: Generates multiple-instance expert persona responses
- `generate_responses_level1S()`: Generates single-instance base responses
- `generate_responses_level2S()`: Generates single-instance persona-based responses
- `generate_responses_level3S()`: Generates single-instance expert persona responses

### Utility Functions
- `make_distribution_length_plot()`: Visualizes distribution of response lengths
- `create_df_answers()`: Creates and saves formatted DataFrames of responses
- `estimate_token_count()`: Estimates token count for API usage optimization

## 📈 Data Analysis Tools

The implementation includes tools for:
- Response length distribution analysis
- Token usage tracking
- Generation time statistics
- Data export to CSV

## 🎛️ Parameters and Configuration

### Adjectives Lists
```python
adjectives_sol = ["highly detailed and elaborate", "succinct", "brief", ...]
adjectives_prob = ["highly detailed and elaborate", "succinct", "brief", ...]
```

### Expert Fields
The implementation includes 23 fields with 5 experts each, covering areas such as:
- Apparel & Textiles
- Automobiles & Tires
- Technology/Hardware Products
- Software & IT Services
- And many more

## 📊 Output Format

The generated data is structured with:
- Problem statements
- Solution descriptions
- Metadata (level, adjectives used, persona if applicable)
- Generation timestamps

## 🚫 Error Handling

The implementation includes:
- Rate limit handling with automatic retries
- Token count management
- Exception logging
- Graceful failure recovery

## 👥 Citation

If you use this code in your research, please cite:

Boussioux, L., Lane, J. N., Zhang, M., Jacimovic, V., & Lakhani, K. R. (2024). The crowdless future? Generative AI and creative problem-solving. *Organization Science*, *35*(5), 1589-1607.

### BibTeX
```bibtex
@article{boussioux2024crowdless,
  title={The crowdless future? Generative AI and creative problem-solving},
  author={Boussioux, L{\'e}onard and Lane, Jacqueline N and Zhang, Miaomiao and Jacimovic, Vladimir and Lakhani, Karim R},
  journal={Organization Science},
  volume={35},
  number={5},
  pages={1589--1607},
  year={2024},
  publisher={INFORMS}
}
```

## 📄 License

MIT License

Copyright (c) 2024 Leonard Boussioux, Jacqueline N Lane, Miaomiao Zhang, Vladimir Jacimovic, Karim R Lakhani
