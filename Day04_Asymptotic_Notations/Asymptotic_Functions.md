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

# Comparing Growth Rates: log(n) vs. n^(1/2)

## **1. Limit Approach**
To compare `log(n)` and `n^(1/2)`, we analyze their growth rates as `n` increases.
We take the limit of their ratio:

$$\lim_{{n \to \infty}} \frac{\log n}{n^{1/2}}$$

Using L'Hôpital's Rule, differentiate the numerator and denominator:

$$\frac{d}{dn} (\log n) = \frac{1}{n}, \quad \frac{d}{dn} (n^{1/2}) = \frac{1}{2 \sqrt{n}}$$

Applying L'Hôpital's Rule:

$$\lim_{{n \to \infty}} \frac{\log n}{n^{1/2}} = \lim_{{n \to \infty}} \frac{1/n}{1/2\sqrt{n}} = \lim_{{n \to \infty}} \frac{2\sqrt{n}}{n} = \lim_{{n \to \infty}} \frac{2}{\sqrt{n}}$$

Since $2 / \sqrt{n} \to 0$ as $n \to \infty$, we conclude:

$$\log n \ll n^{1/2}$$

which means `log(n)` grows much more slowly than `n^(1/2)`.

## **2. Asymptotic Notation**

$$\log n = O(n^{1/2})$$

More precisely,

$$\log n = o(n^{1/2})$$

meaning `log(n)` is asymptotically smaller than `n^(1/2)`.

## **3. Numerical Check**
For small values of `n`:

| `n`     | `log(n)` (base `e`) | `n^(1/2)` |
|---------|---------------------|-----------|
| 10      | 2.3                 | 3.16      |
| 100     | 4.6                 | 10        |
| 1000    | 6.9                 | 31.6      |
| 10,000  | 9.2                 | 100       |

Clearly, `n^(1/2)` grows much faster than `log(n)`.

## **Conclusion**
- `n^(1/2)` grows much faster than `log(n)`.
- For large `n`, `log(n)` is negligible compared to `n^(1/2)`.
- In algorithmic complexity, an `O(sqrt(n))` algorithm is significantly slower than an `O(log n)` algorithm.

🚀 **Big-O Notation Matters!**
