# Detecting Gender Bias in Sentiment and Emotion Classification

To reproduce results one has to put files `users.csv` and `questions.csv` to `data` directory
Additional one has to put LLM classification results to `data/llm` folder

## Preprocessing.ipynb
Combines and cleans data from `users.csv` and `questions.csv`. Output is `data/dataset.csv` file.

## Getting Raw Scores.ipynb
Uses `dataset.csv` to obtain results from various models. These are raw scores, i.e. output of a model as it is. Output is `data/raw_scores_MODELNAME.pkl` files.

## Getting Final Scores.ipynb
Uses raw scores to obtained unified scores, i.e. one of three possible label 'positive', 'negative', or 'neutral'. Output is `data/final_scores_MODELNAME.pkl` files.

## Preprocessing LIWC.ipynb
Separate file to work with LIWC, helps to export data to LIWC and then convert result to final score format. Output is `data/final_scores_liwc.pkl` file.

## Processing LLMs.ipynb
Separate file to convert output of LLMs to final score format. Output is `data/final_scores_MODELNAME.pkl` files.

## Computing errors.ipynb
Computes errors based on final scores. Output is `data/errors.csv` file.

## Plotting data.ipynb
Create plot based on `errors.csv` file. Output is `results.png` file.
