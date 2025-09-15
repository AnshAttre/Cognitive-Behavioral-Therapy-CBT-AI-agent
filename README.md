# Project A Specialized CBT Therapist AI


* **Name:** Ansh Attre
* **University:** Indian Institute Of Technology , Mandi
* **Department:** Data Science and Engineering

## 1. Introduction: From Generalist LLM to a Specialist CBT Therapist

This project  investigates and validates the hypothesis that a general-purpose Large Language Model (LLM) can be transformed into a specialized, therapeutically effective Cognitive Behavioral Therapy (CBT) agent through a meticulous process of fine-tuning and advanced architectural design.

Traditional LLMs often lack the domain-specific depth and structured reasoning required for sensitive applications like mental wellness. Project AURA addresses this by developing a robust AI therapist capable of understanding complex emotional states, identifying cognitive distortions, and providing clinically relevant, empathetic, and context-aware CBT-based guidance. This repository documents the end-to-end scientific journey, from initial experimentation and failures to the successful training and evaluation of the "Ultimate CBT Therapist" AI.

## 2. Key Features & Technologies

Project is engineered with a multi-layered architecture to ensure therapeutic efficacy and conversational coherence:

* **Custom Cognitive Engines:**
    * **`EmotionalIntelligenceEngine`:** A rule-based analyzer for multi-dimensional psychological assessment, detecting sentiment, specific emotions (anxiety, depression), cognitive distortions (e.g., catastrophizing, all-or-nothing thinking), and crisis levels.
    * **`CBTResponseStrategyEngine`:** A hierarchical decision-making module that translates analysis into specific therapeutic strategies (e.g., anxiety-focused, cognitive restructuring, crisis intervention).
* **Fine-tuned LLM Core:**
    * Utilizes **`microsoft/phi-2`**, a small yet powerful LLM, fine-tuned using **QLoRA** for stability and efficiency on resource-constrained environments (e.g., Google Colab's free tier GPU).
* **Retrieval-Augmented Generation (RAG):**
    * Integrated **`RAGKnowledgeEngine`** leveraging **ChromaDB** as a vector store for a curated knowledge base of CBT principles and techniques. This mitigates hallucination and grounds responses in factual therapeutic knowledge.
* **Advanced Prompt Engineering & Model Context Protocol (MCP):**
    * Implements a sophisticated "Separation of Concerns" strategy: training on simplified conversational formats, and dynamically constructing rich, context-aware prompts during inference. This ensures the LLM's responses are clean, guided, and therapeutically aligned.
* **Conversational Memory:**
    * Employs a **`collections.deque`** to maintain a sliding window of conversation history, enabling coherent and continuous dialogue.
* **`UltimateGenerationEngine` (Orchestrator):**
    * The central module that orchestrates the entire pipeline: channeling user input through the cognitive engines, retrieving RAG context, composing dynamic prompts, interacting with the fine-tuned LLM, and post-processing responses.
* **User Interface:**
    * A simple and intuitive web-based interface built with **Gradio**, allowing for interactive demonstrations and testing.

## 3. Project Architecture

The system operates through a meticulously designed flow to ensure every interaction is therapeutically structured.

**Flow Description:**
User input from the Gradio UI is first processed by the `UltimateGenerationEngine`. This orchestrator directs the input through the `EmotionalIntelligenceEngine` for psychological analysis, and the `CBTResponseStrategyEngine` to determine the therapeutic approach. Simultaneously, the `RAGKnowledgeEngine` retrieves relevant CBT knowledge. All this information, along with conversation history, is then used to compose a dynamic prompt for the fine-tuned `Phi-2` LLM. The LLM's raw response undergoes post-processing before being displayed as a polished therapeutic response on the Gradio UI.


```bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name
