# ML Roadmap 2026

A structured 6-month plan to go from solid foundations to interview-ready ML Engineer / Applied Scientist level. Each week cycles through three focus areas: **Foundations → ML Core → Projects + Interview Prep**. The monthly shift is mainly about what you build and how deep you go.

---

## 6-Month Roadmap (Big Picture)

### Month 1 — Strong Foundations + ML Basics
**Topics**
- Python for ML (NumPy, Pandas)
- Math intuition (linear algebra, probability)
- ML basics (regression, classification)
- Evaluation, overfitting

**Deliverable**
- 2 clean notebooks
- 1 mini-project with a GitHub repo

---

### Month 2 — Classic ML That Interviews Love
**Topics**
- Trees + ensembles (Random Forest, XGBoost)
- Feature engineering
- Cross-validation, leakage
- Model debugging

**Deliverable**
- 2 end-to-end ML projects (problem → data → model → metrics → writeup)

---

### Month 3 — Deep Learning Fundamentals
**Topics**
- PyTorch basics + training loop
- CNNs
- Regularization + optimization
- Debugging training

**Deliverable**
- 1 computer vision project
- 1 “from scratch” neural network notebook

---

### Month 4 — NLP + Transformers
**Topics**
- Tokenization
- Attention + transformer basics
- Fine-tuning + evaluation
- Prompt basics

**Deliverable**
- 1 transformer fine-tuning project
- Clear experiment tracking

---

### Month 5 — MLOps + ML System Design
**Topics**
- Data/model versioning
- Pipelines
- Serving + monitoring
- Latency, cost, failure modes

**Deliverable**
- 1 model served via API
- Basic monitoring
- 1 design doc

---

### Month 6 — Interview Domination + Portfolio Polish
**Topics**
- DSA basics (enough for ML roles)
- ML theory revision
- ML system design
- Resume + mock interviews

**Deliverable**
- Polished GitHub
- 2 strong case studies
- Weekly mocks

---

## Step 1 (Weeks 1–2): Build a Strong ML Engineer Base

### Goal of Step 1
Become very comfortable with:
- Python essentials for ML work
- Data handling (NumPy / Pandas)
- Reproducible notebook practice + GitHub hygiene
- Understanding train/validation/test, metrics, and common failure cases

### Time Expectation
- Weekdays: 2–3 hours/day  
- Weekends: 4–5 hours/day  
If you can do more: increase practice time, not topics.

---

## Week 1 — Python + NumPy Fundamentals

### Day 1 (2h): Setup + Repo Workflow
- Install: Python, VS Code, Jupyter, Git
- Create repo: `ml-roadmap-2026`
- Learn: notebooks, Markdown, folder structure
- Output: `01_python_basics.ipynb`

### Day 2 (2–3h): Python Essentials (ML style)
- Functions, loops, list/dict comprehensions
- `collections`, `math`, `random`, `pathlib`
- Writing clean functions (input → output, minimal global state)

### Day 3 (2–3h): Debugging + Code Quality
- Common errors + reading stack traces
- Print/log discipline
- Simple unit tests (minimum needed)

### Day 4 (2–3h): NumPy Core
- Arrays, shapes, broadcasting
- Vectorization (why it’s faster)
- Indexing/slicing

### Day 5 (2–3h): NumPy for ML
- Mean/variance, standardization
- Dot product intuition
- Linear regression prediction in NumPy

### Weekend (4–5h each day): Mini-Project 1
**Dataset:** any CSV (Titanic / Iris / house prices)

**Tasks**
- Load CSV (Pandas allowed)
- Handle missing values
- Split train/test
- Build baseline  
  - Regression: mean prediction  
  - Classification: majority class
- Write results + lessons learned in README

---

## Week 2 — Pandas + EDA + Metrics Basics

### Day 1 (2–3h): Pandas Basics
- DataFrame operations, selecting rows/cols, filtering
- `groupby`, `value_counts`, `merge`
- Missing value handling: `isna`, `fillna`, `dropna`

### Day 2 (2–3h): EDA That Matters
- Target distribution + feature distributions
- Leakage checks (anything that “knows the future”)
- Split strategy intuition

### Day 3 (2–3h): Metrics
**Classification**
- Accuracy, precision, recall, F1
- Confusion matrix

**Regression**
- MAE, MSE, RMSE, R²  
- Choosing metrics and why

### Day 4 (2–3h): First sklearn Pipeline
- `train_test_split`
- Train simple model: Logistic Regression (classification) or Linear Regression (regression)
- Compare against baseline

### Day 5 (2–3h): Writeup + Repo Polish
- Clean notebook
- README: problem, data, approach, results, next steps
- Professional commit history

### Weekend (4–5h each day): Mini-Project 2
**Add**
- Feature engineering (1–2 features)
- Metrics table
- Error analysis (where it fails)
- Explain concepts simply

---

## Concepts You Must Get in Step 1

### 1) Baseline
A baseline is the dumbest reasonable solution.
- Regression: predict mean of training targets
- Classification: predict most frequent class

If the model doesn’t clearly beat baseline, it’s not a real model yet.

### 2) Train / Validation / Test
- Train: learning
- Validation: tuning choices (features, hyperparams)
- Test: final exam, used once

Peeking early inflates performance and gets exposed in interviews.

### 3) Leakage
Leakage happens when the model receives information it won’t have at prediction time:
- Future information
- Target encoded incorrectly
- IDs mapping directly to label

It makes metrics look amazing, then collapses in real usage.

---

## Small Practical Exercises (Notebook Drills)

### Python Drills (10–25 min)
- Write `train_test_split_manual(X, y, test_ratio, seed)`
- Write `accuracy(y_true, y_pred)` without sklearn
- Convert list of dicts → DataFrame → groupby mean

### NumPy Drills
- Standardization per column: `(x - mean) / std`
- Implement MSE loss
- Implement `predict_linear(X, w, b)` using dot product

### Pandas + EDA Drills
- Top 5 categories by count and mean target
- Identify columns with >30% missing values and decide drop/keep
- Build 2 simple features (Titanic example: `family_size = sibsp + parch + 1`)

---

## Free YouTube Resources (Structured)

Pick one per topic to avoid overload.

### Python
- Corey Schafer — Python playlists

### NumPy + Pandas
- freeCodeCamp.org — NumPy/Pandas full courses
- Keith Galli — practical Pandas

### ML Intuition + Metrics
- StatQuest (Josh Starmer)
- 3Blue1Brown — linear algebra intuition

### sklearn Basics
- Sentdex or freeCodeCamp sklearn intros

---

## Biggest Mistake in Step 1
Rushing into fancy models before mastering data + evaluation. Interviews care more about:
- split strategy
- leakage avoidance
- metric choice
- failure debugging

---

## Interview Questions to Practice (Step 1 Topics)
Write answers in 3–6 sentences each:
- Difference between train/validation/test?
- Why is accuracy bad for imbalanced datasets?
- What is leakage? Give 2 examples.
- What is a baseline and why use it?
- Precision vs recall with a real example.
- MAE vs MSE: when to use which?
- What does overfitting look like in metrics?
- How does standardization help some models?
- Difference between `.loc` and `.iloc`?
- Why is NumPy vectorization faster than loops?

---

## Step 1 Output (By Day 14)
Repo should contain:
- 2 notebooks (`01_...`, `02_...`)
- 2 mini-projects with READMEs
- 1 interview answers Markdown file

---

## Step 2 (Weeks 3–6): Master Classical ML Like an Engineer

### Goal of Step 2
By the end of this step you should be able to:
- Use tree-based models (Random Forest, XGBoost)
- Explain bias–variance clearly
- Use proper cross-validation
- Do feature engineering
- Detect and reduce overfitting
- Explain reasoning clearly in interviews

### Time Expectation
- Weekdays: 2–3 hours/day  
- Weekends: 4–5 hours/day  

---

### Week 3 — Bias–Variance + Trees

**Day 1 — Bias vs Variance**
- Train Logistic Regression and a Decision Tree (`max_depth=None`)
- Compare train vs test metrics and identify overfitting

**Day 2 — Decision Trees**
- Train `DecisionTreeClassifier`
- Tune: `max_depth`, `min_samples_split`
- Observe overfitting changes

**Day 3 — Random Forest**
- Compare Decision Tree vs Random Forest
- Observe stability improvements

**Day 4 — Cross-Validation**
- Use `cross_val_score`
- Compare CV score vs single split score

**Weekend Project 1**
- Baseline → Logistic Regression → Decision Tree → Random Forest  
- Add CV + GridSearchCV  
- Write what improved, why, and where it fails

---

### Week 4 — Feature Engineering + Debugging

**Day 1 — Feature Engineering**
- Create 3 new features
- Compare performance change

**Day 2 — Leakage Deep Dive**
- Intentionally add leakage and observe inflated metrics

**Day 3 — Imbalanced Data**
- Compare accuracy vs precision/recall/F1/ROC-AUC

**Day 4 — XGBoost**
- Train XGBoost
- Compare with Random Forest

**Weekend Project 2 (Portfolio-level)**
- Full pipeline + CV + tuning  
- Confusion matrix + error analysis  
- Business interpretation + clean README

---

### Week 5 — Model Understanding

- Feature importance (RF importance, permutation importance)
- Overfitting control (regularization, depth control, early stopping)
- Hyperparameter tuning (grid vs random search)
- Error analysis: where model fails, weakest subgroup, why

---

### Week 6 — Think Like an ML Engineer

- Reproducibility, random seeds
- Simple experiment tracking (CSV/Sheet)
- Refine a final project and compare 5 models
- Document iterative improvements

---

## Step 2 Concepts to Know Deeply
- Bias–variance tradeoff
- Overfitting vs underfitting
- Bagging vs boosting
- Cross-validation
- Feature engineering impact
- Imbalanced metrics
- Hyperparameter tuning strategy

---

## Step 3 (Weeks 7–10): Deep Learning Mastery (PyTorch + Neural Networks)

### Goal of Step 3
By the end of this step you should:
- Understand neural networks (not just use them)
- Write training loops in PyTorch
- Debug exploding/vanishing gradients
- Build a serious CNN project
- Explain backprop in interviews

### Week 7 — NN Foundations (NumPy)
- Activation functions
- Loss functions
- Backprop chain rule intuition
- Weekend: build NN from scratch (NumPy)

### Week 8 — PyTorch Basics + Training Loop
- Tensors, autograd, GPU basics
- Optimizers (SGD, Adam)
- Regularization (dropout, weight decay, batch norm)
- Weekend: MNIST NN project with curves + writeup

### Week 9 — CNNs
- Convolution basics (kernel, stride, padding)
- CNN structure: Conv → ReLU → Pool → FC
- Weekend: CIFAR-10 custom CNN + overfitting fixes + analysis

### Week 10 — Debugging + Transfer Learning
- Detect overfitting + fix
- Vanishing/exploding gradients + fixes
- Learning rate tuning
- Transfer learning + fine-tuning
- Weekend: final CV project with clean training + validation + metrics

---

## Step 4 (Weeks 11–14): Transformers, NLP & LLM Engineering

### Goal of Step 4
By the end of this step you should:
- Understand attention and transformers clearly
- Fine-tune a pretrained model
- Build an embeddings + retrieval system
- Build a mini RAG project
- Evaluate LLM systems (quality, hallucinations, latency)

**Deliverables**
- 1 transformer fine-tuning project
- 1 RAG project with evaluation notes

---

## Step 5 (Weeks 15–18): MLOps + ML System Design

### Goal of Step 5
By the end of this step you should:
- Deploy models via API
- Use basic versioning for reproducibility
- Monitor and reason about drift
- Design ML systems end-to-end with tradeoffs

**Deliverables**
- 1 FastAPI model service
- Dockerized deployment
- Drift simulation + monitoring notes
- 2 ML system design docs

---

## Step 6 (Weeks 19–24): Interview Domination + Portfolio Polish

### Goal of Step 6
By the end of this step you should:
- Answer ML theory questions clearly
- Perform well in ML system design interviews
- Clear ML coding tasks and core DSA rounds
- Present strong project case studies
- Handle mock interviews consistently

**Deliverables**
- 5–7 strong projects in GitHub
- 2 polished case studies
- Regular mock interview routine
- Resume optimized for ML roles

---