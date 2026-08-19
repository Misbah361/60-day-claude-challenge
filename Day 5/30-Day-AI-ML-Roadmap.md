# 30-Day AI/ML Fundamentals Roadmap

**Goal:** Go from zero-to-solid AI/ML fundamentals in 30 days — enough to understand core concepts, build small models, and confidently talk about ML in interviews or on your GitHub.

**Format:** ~1–2 hrs/day. Weekends are lighter (review + project time).

---

## Week 1: Python for Data & Math Foundations

**Milestone:** Comfortable with Python's data stack (NumPy, Pandas) and the core math intuition (linear algebra, stats) behind ML.

| Day | Task | Resource |
|---|---|---|
| 1 | Python refresher: lists, dicts, functions, loops | [Python Official Tutorial](https://docs.python.org/3/tutorial/) |
| 2 | NumPy basics: arrays, broadcasting, vector ops | [NumPy Quickstart](https://numpy.org/doc/stable/user/quickstart.html) |
| 3 | Pandas basics: DataFrames, filtering, groupby | [Pandas 10 Minutes Guide](https://pandas.pydata.org/docs/user_guide/10min.html) |
| 4 | Data visualization: Matplotlib/Seaborn basics | [Matplotlib Pyplot Tutorial](https://matplotlib.org/stable/tutorials/pyplot.html) |
| 5 | Linear algebra intuition: vectors, matrices, dot product | [3Blue1Brown – Essence of Linear Algebra](https://www.3blue1brown.com/topics/linear-algebra) |
| 6 | Stats & probability basics: mean, variance, distributions | [Khan Academy Statistics](https://www.khanacademy.org/math/statistics-probability) |
| 7 | **Weekend project:** Load a real dataset (e.g., Titanic/Iris from Kaggle) and do full EDA (exploratory data analysis) with Pandas + visualizations | [Kaggle Datasets](https://www.kaggle.com/datasets) |

---

## Week 2: Core Machine Learning Concepts

**Milestone:** Understand supervised learning end-to-end and train your first models.

| Day | Task | Resource |
|---|---|---|
| 8 | What is ML? Supervised vs unsupervised vs reinforcement | [Google's ML Crash Course – Intro](https://developers.google.com/machine-learning/crash-course) |
| 9 | Linear regression: theory + implement from scratch | [StatQuest – Linear Regression](https://www.youtube.com/c/joshstarmer) |
| 10 | Logistic regression & classification basics | Google ML Crash Course (Classification module) |
| 11 | Train/test split, overfitting, underfitting, cross-validation | [Scikit-learn Model Selection Docs](https://scikit-learn.org/stable/model_selection.html) |
| 12 | Decision trees & random forests | [StatQuest – Decision Trees](https://www.youtube.com/c/joshstarmer) |
| 13 | Model evaluation: accuracy, precision, recall, F1, confusion matrix | [Scikit-learn Metrics Guide](https://scikit-learn.org/stable/modules/model_evaluation.html) |
| 14 | **Weekend project:** Build a classifier with scikit-learn (e.g., predict Titanic survival or Iris species) end-to-end: clean data → train → evaluate | [Scikit-learn Getting Started](https://scikit-learn.org/stable/getting_started.html) |

---

## Week 3: Neural Networks & Deep Learning Basics

**Milestone:** Understand how neural networks work and train a basic one.

| Day | Task | Resource |
|---|---|---|
| 15 | What is a neural network? Neurons, weights, activation functions | [3Blue1Brown – Neural Networks Series](https://www.3blue1brown.com/topics/neural-networks) |
| 16 | Forward propagation & loss functions | Same series (continue) |
| 17 | Backpropagation & gradient descent intuition | 3Blue1Brown (Backpropagation video) |
| 18 | Intro to PyTorch or TensorFlow/Keras — pick one and stick with it | [PyTorch 60-Min Blitz](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html) |
| 19 | Build a simple neural net on MNIST (handwritten digits) | [Keras MNIST Example](https://keras.io/examples/vision/mnist_convnet/) |
| 20 | Regularization basics: dropout, batch norm (conceptual) | [DeepLearning.AI – Improving Deep Neural Networks](https://www.coursera.org/learn/deep-neural-network) |
| 21 | **Weekend project:** Train and tune a digit classifier on MNIST; document accuracy improvements | Your Week 3 stack |

---

## Week 4: Applied AI, LLMs & Capstone Project

**Milestone:** Understand modern AI tools (LLMs, prompting, APIs) and ship a capstone project.

| Day | Task | Resource |
|---|---|---|
| 22 | What are LLMs? Transformers at a high level (conceptual, no math deep-dive needed) | [Jay Alammar – The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) |
| 23 | Using the Claude/OpenAI API: sending prompts, handling responses | [Anthropic API Docs](https://docs.claude.com) |
| 24 | Prompt engineering fundamentals (builds on your Day 2–4 work!) | [Anthropic Prompt Engineering Guide](https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) |
| 25 | Intro to embeddings & vector search (how semantic search works) | [OpenAI – Embeddings Guide](https://platform.openai.com/docs/guides/embeddings) |
| 26 | Retrieval-Augmented Generation (RAG) concept walkthrough | [Pinecone – What is RAG?](https://www.pinecone.io/learn/retrieval-augmented-generation/) |
| 27 | Plan your capstone: pick a small end-to-end AI project | — |
| 28 | Build capstone (part 1): data + model/API integration | — |
| 29 | Build capstone (part 2): polish, test, document | — |
| 30 | **Capstone demo day:** finalize, write README, push to GitHub, share on LinkedIn | Your `60-day-claude-challenge` repo |

---

## Suggested Capstone Project Ideas (pick one)

- **Sentiment classifier**: Train a scikit-learn model on movie/product reviews, wrap it in a simple Streamlit app.
- **AI-powered chatbot**: Use the Claude API to build a subject-specific Q&A assistant with a simple prompt-engineered system prompt.
- **Digit recognizer app**: Deploy your MNIST model with a simple drawing canvas UI.
- **RAG mini-project**: Build a small "chat with your notes" tool using embeddings + Claude API.

---

## Final Outcome

By Day 30 you will have:
- ✅ A working knowledge of Python's data/ML stack (NumPy, Pandas, scikit-learn)
- ✅ A solid conceptual + practical understanding of supervised learning and neural networks
- ✅ Hands-on experience with a deep learning framework (PyTorch or Keras)
- ✅ Practical LLM/API skills — prompting, embeddings, and RAG concepts
- ✅ A complete, documented capstone project on GitHub
- ✅ A portfolio-ready 30-day journey to show recruiters, on LinkedIn, or to founders/DevRel teams

---

## Tips for Success

- **Document daily** — a short markdown note + screenshot per day keeps momentum (you're already great at this from your 60-day challenge!)
- **Don't skip the math intuition** — even 10 minutes of 3Blue1Brown per concept builds real understanding.
- **Build, don't just watch** — type the code yourself instead of copy-pasting.
- **Weekends = consolidation** — use them to catch up, not to cram new material.
