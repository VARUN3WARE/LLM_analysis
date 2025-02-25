# LLM Models Performance Analysis

This project provides a comprehensive comparison of open-source language models on Groq's platform. We analyze the performance characteristics of multiple language models to help identify the best-fit models for various use cases, considering factors like response quality, speed, resource usage, and cost-efficiency.

## Why We Analyzed This Data

Understanding language model performance is crucial for:

- **Practical Implementation**: Selecting the right model based on response quality, speed, and resource usage.
- **Cost Efficiency**: Balancing token usage and processing time for optimal performance and cost.
- **Response Characteristics**: Investigating how temperature settings affect output length, creativity, and sentiment.
- **Comparative Analysis**: Identifying strengths and weaknesses across different model architectures and sizes.

## How We Collected the Data

We used the **LangChain framework** and **Groq's API** to collect comparative data from five open-source models with different prompts and temperature settings:

### Models Evaluated:
- Llama-3.3-70b
- Gemma2-9b-it
- Llama-3.1-8b
- Mixtral-8x7b
- Qwen-2.5-32b

### Test Prompts:
1. Deep learning explanation
2. What is love?
3. Earning as a 15-year-old
4. AI for climate change

### Temperature Settings:
- **Temperature = 0**: Deterministic
- **Temperature = 1**: Creative

Each model was tested with both temperature settings to observe their effect on response characteristics.

## Dataset Overview

### Basic Metrics:
- **Model Name**: The LLM used for generation
- **Temperature**: 0 or 1 setting
- **Prompt**: The input text provided
- **Content**: The model's generated response

### Performance Metrics:
- **Completion Tokens**: Number of tokens in the response
- **Completion Time**: Time taken to generate the response
- **Prompt Time**: Time to process the input
- **Queue Time**: Wait time before processing

### Derived Metrics:
- **Content Length**: Character count of responses
- **Content Sentiment**: Sentiment score of responses

## Key Insights

- **Token Usage Comparison**: Different models vary in token generation, affecting both cost and response thoroughness.
- **Response Time Analysis**: Larger models tend to take longer, but the relationship between model size and completion time isn’t always linear.
- **Temperature Impact**: Higher temperature settings lead to more diverse responses, with increased token counts and slightly longer response times.
- **Content Length & Sentiment Analysis**: Larger models generate longer responses, with most outputs tending toward a positive sentiment.

## Model Selection Recommendations

- **For Speed-Critical Applications**: Consider smaller models like Llama-3.1-8b or Gemma2-9b for faster responses.
- **For Detailed Responses**: Larger models like Llama-3.3-70b tend to provide more comprehensive answers.
- **For Cost Efficiency**: Mixtral-8x7b offers a good balance of quality and token usage.
- **For Creativity**: Use temperature=1 to increase response diversity.

## Technologies Used
- **Python** (pandas, matplotlib, seaborn, TextBlob)
- **Groq API**
- **LangChain framework**

## License
This project is licensed under the MIT License.
