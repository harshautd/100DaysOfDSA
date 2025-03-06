# Decreasing Functions (Asymptotic Notation)

## **Common Decreasing Functions (Ordered by Rate of Decay)**

### **1. Constant Decay (No Change)**
- **Notation:** `O(1)`
- **Example:** Fixed operations that do not depend on `n`.

### **2. Inverse Logarithmic Decay**
- **Notation:** `O(1 / log n)`
- **Example:** Some probability distributions (e.g., Zipf’s law).

### **3. Inverse Polynomial Decay**
- **Notation:** `O(1 / nᶜ)`, where `c > 0`
- **Examples:**
  - `O(1 / n)` → Harmonic series.
  - `O(1 / n²)` → Inverse square laws (e.g., gravitational force).

### **4. Exponential Decay**
- **Notation:** `O(1 / 2ⁿ)`
- **Example:** Radioactive decay, recursive algorithms with exponential shrinking.

### **5. Factorial Decay**
- **Notation:** `O(1 / n!)`
- **Example:** Taylor series remainder terms.

### **6. Double Exponential Decay**
- **Notation:** `O(1 / 2²ⁿ)`
- **Example:** Extreme cases in combinatorics and cryptography.

## **Ordered List from Slowest to Fastest Decay**
```plaintext
O(1) ≫ O(1 / log n) ≫ O(1 / n) ≫ O(1 / n²) ≫ O(1 / 2ⁿ) ≫ O(1 / n!) ≫ O(1 / 2²ⁿ)
```

## **Real-Life Applications**
| Notation | Example |
|----------|---------|
| `O(1 / log n)` | Zipf’s law, probability distributions |
| `O(1 / n)` | Harmonic series, some economic models |
| `O(1 / n²)` | Gravitational force (inverse square law) |
| `O(1 / 2ⁿ)` | Radioactive decay, dynamic programming optimizations |
| `O(1 / n!)` | Taylor series remainder terms |
| `O(1 / 2²ⁿ)` | Cryptography, theoretical combinatorics |

---
### **Usage in Algorithms & Complexity Analysis**
These functions often appear in probability distributions, physics laws, and optimization problems where the impact of an increase in `n` rapidly diminishes.

---

## **Comparison of Different Growth Rates**
| Type        | Notation | Growth Behavior |
|------------|---------|----------------|
| Constant   | `O(1)` | Stays the same |
| Logarithmic | `O(log n)` | Grows very slowly |
| Linear     | `O(n)` | Grows steadily |
| Quadratic  | `O(n²)` | Grows faster |
| Exponential | `O(2ⁿ)` | Grows extremely fast |
| **Inverse Polynomial** | `O(1 / n)` | Slowly decreases |
| **Exponential Decay** | `O(1 / 2ⁿ)` | Rapidly decreases |
