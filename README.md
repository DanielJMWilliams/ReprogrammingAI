# ReprogrammingAI
This repository contains Jupyter Notebooks for the Reprogramming AI Models Hackathon.

<a href="https://colab.research.google.com/github/DanielJMWilliams/ReprogrammingAI/blob/main/AutoPromptInjection.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# About the repository.
## Setup
To run the notebooks in VS Code, add a .env file to the root folder in the following format:
```
GOODFIRE_API_KEY=Add_Your_Goodfire_API_Key_Here
```


## Repository Structure

- [AutoPromptInjection Notebook](AutoPromptInjection.ipynb) - the Jupyter Notebook with our code.
- The `behaviours` folder contains text lists of words grouped by certain behaviours.
- The `graphs` folder contains our graphed results.

# Report

## Abstract

## Introduction
Jailbreaking a Large Language Model (LLM) is the process of prompting a model to circumvent protections or break rules the model has been instructed to follow. Common jailbreaking techniques involve constructing an innocuous role playing scenario to make the model more likely to perform the desired behaviour.

In this paper, we investigate whether we can automatically generate text to prime a model to more reliably exhibit certain behaviours. 


## Overview

### Method
1. List of behaviours - these are strings
2. Get features related to behaviours
3. Create two variants
	1. Steered positively towards features
	2. Steered negatively away from features
4. Create a dialogue with each variant
5. Construct prompts in format {primer} - {command}
6. Using clear, unsteered model, generate responses with the prompt.
7. Construct prompts in format {primer} - {command}
8. Evaluate whether response contains password.
### Behaviours
We manually created behaviour sets (see appendix). This proved challenging. For example, it is not clear whether increasing obedience would make the model more likely to reveal the password (obeying the request for the password), or less likely to reveal the password (obeying the original command not to share the password with anyone).

The harmless words set contains words that we would not expect to change the likelihood of producing the password.



### Code

## Discussion and Conclusion

## Appendix

behaviours...
