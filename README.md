# 🛒 ShopAssist AI – LLM-Powered Laptop Recommendation System

ShopAssist AI is an **end-to-end intelligent chatbot** that recommends laptops based on user requirements by combining **Large Language Models (LLMs)** with **rule-based decision logic**. The system is designed to be **safe, explainable, and production-ready**, avoiding hallucinations while delivering personalized recommendations.

---

## 📌 Project Overview

Online shoppers often struggle to choose the right laptop due to:

* Too many options
* Lack of personalized assistance
* Unclear technical specifications

**ShopAssist AI** solves this problem by:

* Conversationally gathering user requirements
* Structuring unstructured inputs using LLMs
* Applying deterministic scoring to recommend the **top 3 most suitable laptops**

---

## 🧠 System Architecture

The system is divided into **three major stages**:

### **Stage 1: Intent Understanding**

* Conversational requirement gathering
* Prompt engineering with Chain-of-Thought & Few-Shot prompting
* Intent confirmation to ensure all required attributes are captured
* Safety checks using moderation API

### **Stage 2: Product Mapping & Matching**

* Extracts laptop features from descriptions using LLMs
* Maps features to standardized levels (`low`, `medium`, `high`)
* Rule-based scoring against user requirements
* Budget-based filtering

### **Stage 3: Recommendation & Dialogue**

* Validates recommendation quality
* Presents laptops in a user-friendly format
* Handles follow-up questions conversationally
* Graceful session termination

---

## 🧩 Key Features

* 🔍 **Robust Intent Extraction** from free-text input
* 🛡️ **Safety Guardrails** with moderation checks
* 📐 **Explainable Rule-Based Scoring**
* 🔄 **LLM Consistency Testing**
* 🧾 **Structured Output from Unstructured Data**
* 💬 **Context-Aware Follow-Up Q&A**

---

## 📊 User Attributes Considered

The chatbot captures and validates the following **6 key attributes**:

1. GPU Intensity
2. Display Quality
3. Portability
4. Multitasking Capability
5. Processing Speed
6. Budget (INR)

---

## 🧪 Evaluation

The system was evaluated on three realistic personas:

| Persona                | Description                             | Score |
| ---------------------- | --------------------------------------- | ----- |
| 🎮 Gamer               | High GPU, high display, low portability | 5 / 5 |
| 🎓 Academic Researcher | Computer vision, programming            | 5 / 5 |
| 💼 Business Executive  | High portability, multitasking          | 5 / 5 |

✔ Perfect alignment between inferred and expected requirements across all cases.

---

## 🛠️ Tech Stack

* **Python**
* **OpenAI GPT-3.5 (Chat Completions API)**
* **Pandas**
* **Tenacity (Retry Logic)**
* **Rule-Based Scoring Engine**

---

## 📁 Project Structure

```
├── laptop_data.csv
├── updated_laptop.csv
├── main.ipynb / main.py
├── OPENAI_API_Key.txt
├── README.md
```

---

## 🚀 How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/ShopAssist-AI.git
cd ShopAssist-AI
```

2. Install dependencies

```bash
pip install openai pandas tenacity
```

3. Add your OpenAI API key

```
OPENAI_API_Key.txt
```

4. Run the chatbot

```python
dialogue_mgmt_system()
```

---

## 🔐 Safety & Reliability

* Moderation checks on **user input and model output**
* Intent confirmation before recommendations
* Deterministic logic for final decisions
* No hallucinated specifications

---

## 📈 Future Improvements

* Weighted scoring per user preference
* Battery life and OS as explicit attributes
* Web UI using Flask or Streamlit
* Caching LLM responses for performance
* User feedback loop for continuous learning

---

## 🏁 Conclusion

ShopAssist AI demonstrates how **LLMs and deterministic systems can be combined effectively** to build safe, explainable, and scalable recommendation engines. By restricting LLMs to understanding and extraction, and delegating decision-making to rule-based logic, the system ensures accuracy, transparency, and user trust.

