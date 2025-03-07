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

![equation](https://latex.codecogs.com/png.latex?\lim_{n%20\to%20\infty}%20\frac{\log%20n}{n^{1/2}})

Using L'Hôpital's Rule, differentiate the numerator and denominator:

![equation](https://latex.codecogs.com/png.latex?\frac{d}{dn}%20(\log%20n)%20=%20\frac{1}{n})

![equation](https://latex.codecogs.com/png.latex?\frac{d}{dn}%20(n^{1/2})%20=%20\frac{1}{2%20\sqrt{n}})

Applying L'Hôpital's Rule:

![equation](https://latex.codecogs.com/png.latex?\lim_{n%20\to%20\infty}%20\frac{\log%20n}{n^{1/2}}%20=%20\lim_{n%20\to%20\infty}%20\frac{1/n}{1/2\sqrt{n}}%20=%20\lim_{n%20\to%20\infty}%20\frac{2\sqrt{n}}{n}%20=%20\lim_{n%20\to%20\infty}%20\frac{2}{\sqrt{n}})

Since 2/√n → 0 as n → ∞, we conclude:

![equation](https://latex.codecogs.com/png.latex?\log%20n%20\ll%20n^{1/2})

which means `log(n)` grows much more slowly than `n^(1/2)`.

## **2. Asymptotic Notation**

![equation](https://latex.codecogs.com/png.latex?\log%20n%20=%20O(n^{1/2}))

More precisely,

![equation](https://latex.codecogs.com/png.latex?\log%20n%20=%20o(n^{1/2}))

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

# Comparing log₂n and log₃n Growth Rates

To compare log₂n and log₃n, let's analyze their growth rates.

## 1. Change of Base Formula

Using the logarithm base change formula:
```
log_a(n) = log_b(n) / log_b(a)
```

We can express log₃n in terms of log₂n:
```
log₃n = log₂n / log₂(3)
```

Since log₂(3) ≈ 1.585 > 1, we conclude:
```
log₃n < log₂n
```

for all n > 1.

## 2. Limit Approach

We take the limit of their ratio:
```
lim(n→∞) [log₂n / log₃n]
```

Substituting log₃n = log₂n / log₂(3):
```
lim(n→∞) [log₂n / (log₂n / log₂(3))] = log₂(3) ≈ 1.585
```

Since this is a constant, we conclude:
```
log₂n = Θ(log₃n)
```

which means they grow at the **same rate asymptotically**.

## 3. Asymptotic Notation

Since the ratio converges to a constant, we write:
```
log₂n = Θ(log₃n)
```

which implies that both functions grow at the same rate, up to a constant factor.

## 4. Numerical Comparison

```
| n  | log₂n | log₃n |
|----|-------|-------|
| 2  | 1     | 0.631 |
| 4  | 2     | 1.262 |
| 8  | 3     | 1.893 |
| 16 | 4     | 2.524 |
| 32 | 5     | 3.155 |
```

Clearly, log₂n is always larger, but they both grow **slowly and proportionally**.

## If the leading terms of two functions differ only by a constant factor, then Big-O (O), Big-Omega (Ω), and Theta (Θ) notations can be applied.
