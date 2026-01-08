# kNN & Distance-Based Learning — FAANG-Level Hands-On

**Goal:** Build strong intuition for kNN, distance metrics, curse of dimensionality, and bias–variance tradeoffs.

**Outcome:** Students can implement kNN from scratch (vectorized), reason about metric choice, and explain failure modes at FAANG interview depth.

---

# How to Start

1. **Fork** this repository.  
2. Open `knn_student_lab.ipynb` in **Google Colab**.  
3. Complete all **TODO** sections.  
4. **Restart runtime → Run All** cells.  
5. Push changes and submit a **Pull Request**.  

⚠️ **Do NOT edit notebooks directly on GitHub.**

---

## Lab Rules (FAANG Style)

- ✅ Avoid Python loops over samples when vectorization is possible
- ✅ Track complexity: kNN is expensive at inference
- ✅ Explain metric choice and scaling
- ✅ Always evaluate under different k

---

# Out of Scope

- Approximate nearest neighbors (FAISS) (covered later)
- Production indexing systems

---

# Notebook Rules

- Do **NOT** rename the notebook  
- Do **NOT** delete TODOs  
- Do **NOT** hardcode outputs  
- Notebook must run **top-to-bottom**  

---

# Dataset

- Synthetic classification datasets with controllable dimension

## Why?

- Lets us demonstrate curse of dimensionality cleanly
- Mirrors interview settings

---

## Section 1 — Distance Metrics

### Task 1.1: Implement vectorized L2 distances

Compute distance matrix between X_test (m,d) and X_train (n,d) without loops.

**Checkpoint Questions:**

- What is the complexity of computing all pairwise distances?
- Why can broadcasting blow up memory?

---

### Task 1.2: Compare L1 vs L2

**Interview Angle:**

- When might L1 be preferred to L2?

---

## Section 2 — kNN Classifier

### Task 2.1: Implement kNN predict

- Find k nearest neighbors
- Majority vote

**FAANG Gotcha:**

- Ties and deterministic tie-breaking

---

### Task 2.2: Evaluate k sweep

- Show train vs test accuracy for k in [1,3,5,9,15]

**Checkpoint Questions:**

- Why does k control bias vs variance?

---

## Section 3 — Curse of Dimensionality

### Task 3.1: Distance concentration experiment

- Fix n samples
- Increase d
- Show ratio (min_dist / max_dist) approaches 1

**Interview Angle:**

- Why does kNN degrade in high dimensions?

---

## Section 4 — Feature Scaling

### Task 4.1: Show kNN sensitivity to scaling

- Create a feature with large scale
- Show accuracy drop
- Fix with standardization

---

## Submission Expectations

- Completed notebook
- Answers to checkpoint questions
- Short complexity notes (time/memory)

---

## FAANG Interview Evaluation Rubric

| Skill                        | Evaluated |
|-----------------------------|-----------|
| Vectorization               | ✅        |
| Complexity reasoning        | ✅        |
| Metric/scaling intuition    | ✅        |
| Bias–variance explanation   | ✅        |
| Code clarity                | ✅        |

---

## Stretch Problems (Optional)

- Weighted kNN
- Distance-weighted voting vs majority vote
- kNN regression
