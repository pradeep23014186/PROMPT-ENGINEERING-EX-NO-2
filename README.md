<h1 align="center"> EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization </h1>

# AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

# Procedure:
## 1. Zero-Shot Prompting
- **Definition:** Asking the model to perform the task without examples or reasoning guidance.
  
- **Strengths:** Fast, simple, and effective for short, factual texts.
  
- **Weaknesses:** May produce generic or uneven quality summaries.  

**Example Prompt:**
```
Summarize a 500-word technical article on ‘How AI changed Indian Agriculture’ in 150 words for undergraduate students.
```

## 2. Few-Shot Prompting
- **Definition:** Providing examples of desired outputs before asking for the task.
  
- **Strengths:** Improves consistency, tone, and domain-specific accuracy.
  
- **Weaknesses:** Requires careful example selection; longer prompts may reduce efficiency.  

**Example Prompt:** 
```
Here are some examples of how to explain complex topics:

- Topic: Photosynthesis
- Explanation: Photosynthesis is the process by which plants convert sunlight, water, and carbon dioxide into energy and oxygen.

- Topic: Gravity
- Explanation: Gravity is the force that pulls objects toward each other, like how the Earth pulls us to its surface.

Now explain: How AI changed Indian Agriculture.
```
## 3. Chain-of-Thought (CoT) Prompting
- **Definition:** Asking the model to reason step-by-step before summarizing.  

- **Strengths:** Useful for complex, multi-layered texts (legal, scientific, policy).  

- **Weaknesses:** Can be slower and sometimes overly detailed.  

**Example Prompt:**
```
Summarize a 500-word technical article on ‘How AI changed Indian Agriculture.’ First, identify the main themes (e.g., crop monitoring, predictive analytics, supply chain). Then, explain how AI impacts each theme. Finally, write a concise 150-word summary for undergraduate students.
```

## 4. Role-Based Prompting
- **Definition:** Assigning the model a persona (e.g., “You are a journalist summarizing for a newspaper”).
  
- **Strengths:** Produces highly tailored, audience-specific summaries.
  
- **Weaknesses:** Risk of bias if role is too narrowly defined.

**Example Prompt:**
```
You are an educational content curator for undergraduate students. Your task is to summarize a 500-word technical article on ‘How AI changed Indian Agriculture’ in 150 words, using simple language, clear structure, and examples relevant to students.
```
# Importance of prompt evaluation:
- **Quality assurance** – Evaluating prompts helps make sure that your AI applications consistently produce high-quality, relevant outputs for the selected model.
  
- **Performance optimization** – By identifying and refining effective prompts, you can improve the overall performance of your generative AI models in terms of lower latency and ultimately higher throughput.
  
- **Cost efficiency** – Better prompts can lead to more efficient use of AI resources, potentially reducing costs associated with model inference. A good prompt allows for the use of smaller and lower-cost models, which wouldn’t give good results with a bad quality prompt.
  
- **User experience** – Improved prompts result in more accurate, personalized, and helpful AI-generated content, enhancing the end user experience in your applications.
  
## Evaluation Metrics Architecture:
<img width="1600" height="1273" alt="image" src="https://github.com/user-attachments/assets/68f96e0f-0f2d-4451-9321-7f293660f2d4" />

## Evaluation Framework
**AI platforms used:**
- Microsoft Copilot
  
- OpenAI ChatGPT
  
- Anthropic Claude
  
- Google Gemini

**Each combination (Prompting Technique × Platform) is rated on:**

- Accuracy (faithfulness to source)

- Coherence (logical flow)

- Simplicity (ease of understanding for undergraduates)

- Speed (response time)

- User Experience (clarity, formatting, tone)

## Comparison Table

| Platform      | Prompt Type      | Accuracy | Coherence | Simplicity | Speed | UX | Avg |
|---------------|------------------|----------|-----------|------------|-------|----|-----|
| Copilot       | Zero-Shot        | 4        | 4         | 3          | 5     | 4  | 4.0 |
| Copilot       | Few-Shot         | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Copilot       | Chain-of-Thought | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Copilot       | Role-Based       | 5        | 5         | 5          | 4     | 5  | 4.8 |
| ChatGPT       | Zero-Shot        | 4        | 4         | 4          | 5     | 4  | 4.2 |
| ChatGPT       | Few-Shot         | 5        | 5         | 4          | 4     | 5  | 4.6 |
| ChatGPT       | Chain-of-Thought | 5        | 5         | 4          | 4     | 5  | 4.6 |
| ChatGPT       | Role-Based       | 5        | 5         | 5          | 4     | 5  | 4.8 |
| Claude        | Zero-Shot        | 4        | 4         | 4          | 4     | 4  | 4.0 |
| Claude        | Few-Shot         | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Claude        | Chain-of-Thought | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Claude        | Role-Based       | 5        | 5         | 5          | 4     | 5  | 4.8 |
| Gemini        | Zero-Shot        | 4        | 4         | 3          | 5     | 4  | 4.0 |
| Gemini        | Few-Shot         | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Gemini        | Chain-of-Thought | 5        | 5         | 4          | 4     | 5  | 4.6 |
| Gemini        | Role-Based       | 5        | 5         | 5          | 4     | 5  | 4.8 |

---
## Bar chart Comparison:
<img width="2000" height="1200" alt="image" src="https://github.com/user-attachments/assets/8c73beab-1e19-4b25-afe5-d6661dbdafbc" />

## Radar Chart Comparison:
<img width="1400" height="1400" alt="image" src="https://github.com/user-attachments/assets/b8391a8c-b382-4bca-ae19-53c3f36b4105" />

# Conclusion
- **Role-Based Prompting consistently scores highest** across platforms (avg ~4.8).  
- **Few-Shot and Chain-of-Thought** are nearly tied, both strong for technical summarization.  
- **Zero-Shot** works but tends to be less tailored and slightly less simple. 
