
This project fine-tunes facebook/opt-1.3b using LoRA-based Supervised Fine-Tuning (SFT) on the FinGPT Financial Sentiment dataset in order to enable **financial sentiment analysis**: given a piece of financial news or report, the model predicts its sentiment (positive/ neutral/ negative).

## Dataset

The dataset used is `fingpt-sentiment-train`, which contains ≈ 76.8k samples.  
Each sample includes:
- an `instruction` (prompt for sentiment classification),  
- an `input` (financial text),  
- and an `output` (sentiment label: positive / neutral / negative).  

Find more details about the dataset [here](https://huggingface.co/datasets/FinGPT/fingpt-sentiment-train) on HuggingFace.

## Training Pipeline

1. Load the `fingpt-sentiment-train` using `datasets`
2. Preprocess the dataset into SFT format
3. Load `facebook/opt-1.3b` using `transformers` as the base model
4. Apply LoRA from `peft` for parameter-efficient training
5. Train using `SFTTrainer` from `trl`
6. Save both the LoRA adapter and merged model
