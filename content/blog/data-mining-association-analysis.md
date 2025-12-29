---
title: Data Mining & Association Analysis
date: 2025-12-29T12:45:57.515Z
---

# Data Mining & Association Analysis – Answers

---

## **1. Answer the following with proper explanation**

### **a) Impact of Normalization in Data Preprocessing**
Normalization rescales data into a common range (e.g., 0–1 or −1 to 1).

**Impact:**
- Prevents attributes with large values from dominating
- Improves performance of distance-based algorithms (k-means, k-NN)
- Speeds up convergence of machine learning models
- Ensures fair comparison among features

**Example:**  
Income (₹10,000–₹1,000,000) and Age (1–100).  
Without normalization, income dominates distance calculations.

---

### **b) Does FP-Growth Maintain Downward Closure Property?**
Yes, **FP-Growth maintains the downward closure property implicitly**.

**Explanation:**
- Downward closure: If an itemset is frequent, all its subsets must be frequent
- FP-Growth avoids candidate generation
- It uses conditional FP-trees to ensure only frequent subsets are explored

**Search Space Reduction:**
- No candidate generation
- Compact FP-tree structure
- Recursive mining on conditional databases

---

### **c) What is a Null Transaction? How Does Cosine Similarity Reduce Its Impact?**
A **null transaction** is a transaction where none of the items under comparison appear.

**Problem:**
- Null transactions increase similarity artificially in some measures

**Cosine Similarity:**
\[
\text{Cosine}(A,B) = \frac{A \cdot B}{|A||B|}
\]

**Advantages:**
- Ignores transactions where both items are absent
- Focuses only on co-occurrence
- Reduces noise from null transactions

---

## **2. Chi-Square Test and Association Rule**

### **Given Contingency Table**

| Gender | Yes | No | Total |
|------|-----|----|------|
| Male | 90 | 170 | 260 |
| Female | 250 | 50 | 300 |
| Total | 340 | 220 | 560 |

---

### **a) Chi-Square Test**
**Null Hypothesis (H₀):** Gender and bird lover are independent  
**Alternative Hypothesis (H₁):** Gender and bird lover are correlated

**Expected Frequency Formula:**
\[
E = \frac{(Row\ Total \times Column\ Total)}{Grand\ Total}
\]

Expected values:
- Male–Yes = 157.86
- Male–No = 102.14
- Female–Yes = 182.14
- Female–No = 117.86

\[
\chi^2 = \sum \frac{(O - E)^2}{E}
\]

\[
\chi^2 = 138.61
\]

**Degrees of Freedom:** (2−1)(2−1) = 1  
**Critical Value (α = 0.05):** 3.84  

**Decision:**  
138.61 > 3.84 ⇒ Reject H₀  

**Conclusion:**  
Gender and bird lover are correlated.

---

### **b) Association Rule: Female → Yes**

- Support = 250 / 560 = **44.64%**
- Confidence = 250 / 300 = **83.33%**

**Thresholds:**
- Minimum Support = 50%
- Minimum Confidence = 60%

**Conclusion:**  
Rule is **not strong** because it fails minimum support condition.

---

## **3. FP-Tree Construction (Min Support = 50%)**

### **Transaction Dataset**

T1: P Q R S T  
T2: P S T X  
T3: T  
T4: X Y Z  
T5: P S T  

---

### **Step 1: Item Frequency Count**

| Item | Count |
|----|----|
| T | 4 |
| P | 3 |
| S | 3 |
| X | 2 |
| Q | 1 |
| R | 1 |
| Y | 1 |
| Z | 1 |

Minimum support count = 50% of 5 = **3**

Frequent items: **T, P, S**

---

### **Step 2: Remove Infrequent Items & Sort**

T1: P S T  
T2: P S T  
T3: T  
T4: — (removed)  
T5: P S T  

---

### **Step 3: FP-Tree Construction**

Root
└── T:4
└── P:3
└── S:3

---

## **4. Mining Frequent Patterns (Min Support = 50%)**

### **Frequent Itemsets**

**Single Items:**
- {T}, {P}, {S}

**Two-Item Sets:**
- {T,P}, {T,S}, {P,S}

**Three-Item Set:**
- {T,P,S}

---

### **Final Frequent Patterns**
{T}  
{P}  
{S}  
{T,P}  
{T,S}  
{P,S}  
{T,P,S}

---
