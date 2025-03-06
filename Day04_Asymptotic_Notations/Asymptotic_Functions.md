# Decreasing Functions (Asymptotic Notation)

## **Common Decreasing Functions (Ordered by Rate of Decay)**

### **1. Constant Decay (No Change)**
- **Notation:** `O(1)`
- **Example:** Fixed operations that do not depend on `n`.

### **2. Inverse Logarithmic Decay**
- **Notation:** `O(1 / log n)`
- **Example:** Some probability distributions (e.g., Zipf’s law).

### **3. Inverse Polynomial Decay**
- **Notation:** `O(1 / n^c)`, where `c > 0`
- **Examples:**
  - `O(1 / n)` → Harmonic series.
  - `O(1 / n^2)` → Inverse square laws (e.g., gravitational force).

### **4. Exponential Decay**
- **Notation:** `O(1 / 2^n)`
- **Example:** Radioactive decay, recursive algorithms with exponential shrinking.

### **5. Factorial Decay**
- **Notation:** `O(1 / n!)`
- **Example:** Taylor series remainder terms.

### **6. Double Exponential Decay**
- **Notation:** `O(1 / 2^{2^n})`
- **Example:** Extreme cases in combinatorics and cryptography.

## **Ordered List from Slowest to Fastest Decay**
```plaintext
O(1) ≫ O(1 / log n) ≫ O(1 / n) ≫ O(1 / n^2) ≫ O(1 / 2^n) ≫ O(1 / n!) ≫ O(1 / 2^{2^n})
```

## **Real-Life Applications**
| Notation | Example |
|----------|---------|
| `O(1 / log n)` | Zipf’s law, probability distributions |
| `O(1 / n)` | Harmonic series, some economic models |
| `O(1 / n^2)` | Gravitational force (inverse square law) |
| `O(1 / 2^n)` | Radioactive decay, dynamic programming optimizations |
| `O(1 / n!)` | Taylor series remainder terms |
| `O(1 / 2^{2^n})` | Cryptography, theoretical combinatorics |
