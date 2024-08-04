# MSBA-316-NLP-Project-CoCoT
CoCoT (Coding Companion Tutor) - A chatbot designed for Python programming tutoring

## Abstract
As coding has become one of the most important skills for competing in today’s diverse workplaces and research fields, many students are required or motivated to learn it. However, challenges such as time constraints, financial limitations, and the inherent difficulty of programming can make it difficult to acquire these skills. To address these challenges, we developed CoCoT (Coding Companion Tutor), a chatbot designed to combine teaching qualities with programming expertise, specifically aimed at tutoring Python due to its simplicity for beginners. Following its development, we assessed its effectiveness in teaching Python programming through both internal evaluation and human-subject testing. Results showed CoCoT's strong ability in teaching Python, demonstrating significant improvement over the original base model, and high user satisfaction according to human-subject feedback.

## Dataset
To fine-tune our model, we selected three different datasets, each contributing to one or more aspects that we wanted to incorporate into our chatbot. All dataset are sourced from HuggingFace.
- Dataset 1: codefuse-ai/CodeExercise-Python-27k
- Dataset 2: ibl-best-practices-instructor-dataset
- Dataset 3: KrisPi/PythonTutor-Evol-1k-DPO-GPT4-vs-35

The datasets were then combined and preprocessed for efficient finetuning.

## Base Model Selection
We selected LLaMA-3 8b as our base model for developing CoCoT.

## Running the notebooks
The repository contains four notebooks, which were run on Google Colab.
- `Training_and_Evaluation.ipynb` runs the fine-tuning process of base model LLaMA-3 8b on the prepared dataset.
- `Implementation.ipynb` implements the chatbot using LangChain for conversational AI, and creates a UI using Gradio for user interactions.
- `Logical_Inference_LLMAgent.ipynb` implemnts an LLM Agent using LangChain that integrates three different inference tools into a language model.
- `Rule_based_System_Trial(Pyke).ipynb` implements a rule-based system and an attempt to integrate it with a language model, however this integration it is not functionional.
  
Each notebook provides comprehensive details on all performed steps.

Please note that you must specify the correct path to the saved fine-tuned model to ensure the proper execution of each notebook.

## Results
Progression of training loss over training steps:

<img src="https://github.com/malakslim/MSBA-316-NLP-Project-CoCoT/blob/main/training_loss.PNG" style="width: 50%;">


Average results obtained from human-subject evaluation over 5 subjects:

<img src="https://github.com/malakslim/MSBA-316-NLP-Project-CoCoT/blob/main/human-subject.png" style="width: 50%;">

Example prompt comparing responses from the original LLaMa-3 8b model and CoCoT:

### For any further details, please refer to the [PDF report](https://github.com/malakslim/EECE798K-Project/blob/main/EECE_798K_Project_Report.pdf).


