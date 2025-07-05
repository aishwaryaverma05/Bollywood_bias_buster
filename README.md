Bollywood Bias Buster: Simple Plot Analysis for Gender Stereotypes
Project Overview
This project implements a quick, rule-based method to identify potential gender stereotypes in Bollywood movie plots. It analyzes plot summaries to detect the presence of male-associated professional keywords versus female-associated relational/descriptive keywords, flagging plots that lean heavily towards traditional female roles.

This project serves as a basic illustration of how computational analysis can be applied to cultural content to highlight subtle biases.

How It Works
The core logic is a simple keyword-based detection:

Data Loading: Sample movie titles and their plot summaries are loaded into a Pandas DataFrame.

Keyword Definition: Pre-defined lists of keywords are used to represent typical "male" professions (e.g., 'engineer', 'doctor', 'soldier') and "female" relational/descriptive roles (e.g., 'daughter', 'wife', 'beautiful').

Bias Detection Function: A Python function iterates through each plot, counts the occurrences of male and female keywords.

Bias Flagging: If the count of female-associated keywords is significantly higher than male-associated keywords in a plot, it's flagged as having "⚠️ Potential gender stereotype detected". Otherwise, it's marked as "✅ Balanced or male-profession focused".

Getting Started
Prerequisites
To run this notebook, you will need:

Python 3.x

Jupyter Notebook or JupyterLab

pandas library

textblob library (for sentiment analysis, though not fully utilized in the current bias detection logic, it's imported)

Installation
Clone the repository:

git clone [Link to your GitHub Repository for this project]
cd [your-repository-name]

Install necessary Python packages:

pip install pandas textblob

Usage
Open the Jupyter Notebook:

jupyter notebook bollywood_bias_buster.ipynb

Run all cells: Execute the cells sequentially to see the bias detection in action on the sample data.

Modify Data: You can modify the data dictionary in the notebook to add more movie plots for analysis.

Customize Keywords: Feel free to expand or modify the male_keywords and female_keywords lists to refine the bias detection.

Code Structure
Import Libraries: pandas, re (regular expressions), textblob (for NLP, specifically sentiment, though not used in current bias logic), IPython.display.

Data Loading: A dictionary data converted into a pandas DataFrame df.

Keyword Definitions: male_keywords and female_keywords lists.

detect_bias Function: The core logic for identifying stereotypes.

Application: df['plot'].apply(detect_bias) applies the function to each movie plot.

Results Display: Loops through the DataFrame to print results in Markdown format.

Limitations
Rule-Based Simplicity: This is a very basic rule-based approach. It doesn't understand context, sarcasm, or nuances of language. It relies solely on keyword matching.

Limited Keyword Set: The effectiveness is highly dependent on the chosen keywords. A more comprehensive analysis would require extensive linguistic resources.

Binary Output: The output is a simple "potential stereotype" or "balanced," which might oversimplify complex thematic representations.

No NLP for Deeper Meaning: It doesn't leverage advanced Natural Language Processing (NLP) techniques (like entity recognition or deeper sentiment analysis) to understand roles or relationships beyond simple keyword presence.

Future Enhancements (Ideas)
Integrate more sophisticated NLP models (e.g., SpaCy, NLTK for part-of-speech tagging, named entity recognition) to identify roles more accurately.

Expand keyword lists significantly or use word embeddings for semantic similarity.

Incorporate sentiment analysis (from TextBlob or other libraries) to analyze how characters are described.

Gather a larger, more diverse dataset of movie plots for better analysis.

Develop a more nuanced scoring system instead of a binary flag.
