# Sentiment Analysis with Mistral 7B Instruct

This project utilizes the Mistral 7B Instruct model for sentiment analysis on movie reviews. Through an API via KoboldCpp, the model is accessible remotely, enabling integration into cloud-based platforms such as Google Colab.

### Model Details and Setup
The project uses the Mistral-7B-Instruct-v0.1-GPTQ, a compact and efficient LLM suitable for instruction-based tasks. The 4-bit quantized version balances performance with processing speed, ideal for complex text analysis. Detailed information about the model is available on [Hugging Face](https://huggingface.co/TheBloke/Mistral-7B-v0.1-GPTQ).

The model runs on a local server and is accessible via a remote API tunnel provided by KoboldCpp, facilitating both local and cloud-based applications.

### Dataset and Analysis Workflow
The dataset consists of movie reviews, each labeled as positive or negative. The analysis workflow includes:
- **Data Loading**: Reviews are loaded into a pandas DataFrame.
- **Text Cleaning**: Non-alphabetic characters are removed, and crucial punctuation is retained to maintain sentiment integrity.
- **Tokenization**: Reviews are tokenized and stopwords are removed, focusing on the significant words that convey sentiment.

### Sentiment Prediction and Performance Metrics
Sentiments are predicted using specific, instruction-based prompts through the KoboldCpp API with the Mistral model. The configuration uses a low temperature of 0.1, top P of 0.2, and a max length of 2 for precise and relevant outputs. Metrics such as **accuracy (94.7368%), precision (97.6898%), recall (91.6409%),** and **F1 Score (94.5687%)** demonstrate the model's effectiveness.

