Assignment 3: Building a Simple Transformer for Text Classification
Dataset: IMDb Movie Reviews (Sentiment Analysis)
Assignment Overview (25%)
In this assignment, you will implement a simplified Transformer model from scratch to perform sentiment analysis on the IMDb Movie Reviews dataset. You will learn the core building blocks of Transformer-based architectures, such as self-attention and positional encodings, and apply these concepts to a practical text classification task.

This assignment emphasizes understanding the mechanics of Transformers, including the attention mechanism and multi-head attention. Prebuilt Transformer libraries (e.g., Hugging Face Transformers) cannot be used.

About the IMDb Dataset
The IMDb dataset is a popular benchmark dataset for binary sentiment analysis. It consists of movie reviews labeled as positive or negative.

Dataset Description
Features (Input): Movie reviews (text data)
Target (Output): Sentiment labels:
Positive (1)
Negative (0)
Dataset Properties:
Number of Samples: 50,000
Training Set: 25,000 reviews
Test Set: 25,000 reviews
Balanced Dataset: Equal numbers of positive and negative samples.
Learning Goals
By completing this assignment, you will:

Understand Core Transformer Concepts:

Learn the mechanics of self-attention and multi-head attention.
Understand the role of positional encodings in processing sequential data.
Implement a Simplified Transformer:

Build key components of a Transformer, including the attention mechanism, feedforward layers, and positional encoding.
Train and Evaluate the Model:

Train the Transformer model on the IMDb dataset for sentiment classification.
Evaluate the model’s performance using accuracy and other relevant metrics.
Assignment Tasks
1. Transformer Implementation 
Architecture Requirements: All of the following components must be implemented from scratch using numpy, or torch. 

Input Embedding Layer:
Convert input text to token embeddings using a simple word embedding layer.
Use torch.nn.Embedding or implement your own.
Positional Encoding:
Add positional encodings to input embeddings to incorporate sequential information.
Self-Attention Mechanism:
Implement scaled dot-product attention: 
Use multi-head attention for richer feature representations.
Feedforward Network:
Add a two-layer feedforward network with ReLU activation.
Classification Head:
Use a fully connected layer to map the output of the Transformer to a binary label (positive or negative).
Architecture Summary:
Input → Embedding → Positional Encoding → Multi-Head Attention → Feedforward → Classification Head → Output
Forward Propagation:

Implement tokenization, embedding, attention computation, and feedforward operations.
Use softmax activation in the output layer for binary classification probabilities.
Backward Propagation:

Compute gradients for all weights using binary cross-entropy loss.
Update weights using Adam Optimizer.
Training Loop:

Train the Transformer for 10 epochs with:
Batch size: 32
Learning rate: 0.001
Use mini-batch processing.
Evaluation:

Evaluate the model on the IMDb test set.
Calculate and report accuracy, precision, recall, and F1-score.
2. Dataset Handling 
Load the IMDb dataset using datasets from huggingface only. Do not use TensorFlow and Keras.
Preprocess the data using torchtext: 
Tokenize text into words or subwords.
Pad sequences to a uniform length.
Split the original training data into training (80%) and validation (20%) subsets.
Questions 
Understanding Attention:

Explain how the self-attention mechanism works and why it is important for sequence-based tasks.

Analyzing Model Performance:

If your model achieves poor accuracy, identify two potential reasons and suggest solutions.

Deliverables
Code Submission:

A Python file or Jupyter Notebook implementing the Transformer.
Ensure your code is modular, well-commented, and functional.
Report Submission:

Answers to the provided questions.
A brief summary of your implementation, challenges faced, and solutions applied.
Results, including:
Training and validation loss over epochs.
Accuracy, precision, recall, and F1-score on the test set.
Others: See submission requirements.
Sample Expected Results
Training Output:
Epoch 1/10 - Loss: 0.48, Accuracy: 0.76
Epoch 10/10 - Loss: 0.22, Accuracy: 0.89
Evaluation Metrics:
Test Accuracy: 0.88
Precision: 0.87
Recall: 0.89
F1-Score: 0.88
The model is expected to achieve an accuracy of 80%–90% on the IMDb test set to achieve "Good" or "Excellent".

Submission Requirements
Code Submission:

Submit a Python file or Jupyter Notebook with your implementation. Please do not submit a zip file.
Ensure your code is modular, well-commented, and functional.
Name your report (pdf) and notebook as follows: "assignment-3_your-first-name_stuID".
Report:

Include answers to the questions.
Provide a concise and solid report with:
A summary and explanation of your implementation, data processing, and model selection (e.g. how to select the best model) to help others understand your work.
Result analysis and visualization, including training and test accuracy, findings, insights, or interesting observations.
Challenges faced and solutions applied, including evidence or supporting data to support your statement. Please focus on challenges related to model training efficiency and performance. Results and experiments (code) are required to demonstrate the effectiveness of the proposed solutions.
Answers to the questions. 
AI use statement.
Resources
IMDb DatasetLinks to an external site.
Recommended Libraries: numpy, torch, torchtext, matplotlib.
Generative AI (GenAI) Use for This Assignment
You may use Generative AI tools (e.g., ChatGPT or similar) as a learning and writing support tool, but not as a replacement for your own work.

Permitted uses

You may use GenAI for:

Brainstorming and planning: generating ideas, outlining your response, or suggesting ways to structure an argument.
Clarifying understanding: asking questions to help you understand concepts from lectures/tutorials (e.g., “Explain X in simple terms”, “What is the intuition behind Y?”).
Language polishing: improving grammar, clarity, and academic tone without changing the substance of your work.
Checking your own work: identifying unclear wording, logical gaps, or places where additional justification is needed.
Not permitted

You must not use GenAI to:

Generate the final answer (in whole or in part) and submit it as your own work.
Produce complete solutions to questions (including full explanations, derivations, or calculations) that you then copy into your submission with minimal changes.
Create or invent citations/references or claim sources you have not actually consulted.
Bypass learning activities by asking the tool to “do the assignment” (e.g., “Write my answer to Q1”, “Solve Q3 step-by-step and give the final answer”).
Required disclosure (AI use statement)

If you use GenAI in any way, include a short AI use statement at the end of your submission, describing:

the tool(s) used,
what you used it for (e.g., brainstorming, concept clarification, language editing),
and (optionally) one or two example prompts you used.
Example AI use statement (acceptable):
“I used ChatGPT for brainstorming an outline for Q2 and for language polishing. I also asked clarification questions about mutual information to check my understanding. All final content, calculations, and references are my own”.

Reminder: You are responsible for the correctness of all content, calculations, and references submitted.

End of Assignment