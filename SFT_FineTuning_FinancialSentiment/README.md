
This project fine-tunes a large language model (LLM) using the **fingpt-sentiment-train** dataset, and the **LoRA** method in order to enable **financial sentiment analysis**: given a piece of financial news or report, the model predicts its sentiment (positive/ neutral/ negative).

## Dataset

The dataset used is `fingpt-sentiment-train`, which contains ≈ 76.8k samples.  
Each sample includes:
- an `instruction` (prompt for sentiment classification),  
- an `input` (financial text),  
- and an `output` (sentiment label: positive / neutral / negative).  

Find more details about the dataset [here](https://huggingface.co/datasets/FinGPT/fingpt-sentiment-train).  
