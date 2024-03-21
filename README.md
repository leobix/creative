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

## Key Insights From Code **

The Power of Prompt Engineering: Discover how different prompt engineering strategies influence the quality and relevance of GPT-4's output.
Recent studies hint at the tendency of LLMs, like GPT-4, to produce homogenized outputs, potentially stifling the diversity of creative solutions. To address this, we've devised and tested two innovative configurations of GPT-4 aimed at boosting the variety of generated ideas:

1. **Multiple-Instance Solutions**: This setup leverages separate instances of GPT-4, each tasked with generating a unique solution based on the same prompt. This method takes advantage of the LLM's sampling techniques to ensure a broad spectrum of responses, despite identical inputs.

2. **Single-Instance Solutions with Differentiation Instructions**: Here, a single GPT-4 instance generates multiple, distinct solutions in sequence, guided by instructions to diversify outputs. This approach simulates an iterative brainstorming process, pushing the boundaries of creativity and uniqueness in solution generation.

Let's build a better future! 🌍
