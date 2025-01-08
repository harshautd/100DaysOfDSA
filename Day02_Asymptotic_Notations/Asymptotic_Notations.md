
| Notation     | Definition                                                                 | Example (f(n) and g(n))           | Diagram Description                         |
|--------------|-----------------------------------------------------------------------------|------------------------------------|---------------------------------------------|
| **Big-O**    | f(n) ≤ c * g(n) for large n, for some constant c > 0.                      | f(n) = 3n² + 2n + 1, g(n) = n³    | f(n) is below or equal to g(n) asymptotically. |
| **Small-o**  | f(n) < c * g(n) for large n, for all constants c > 0.                      | f(n) = 3n² + 2n + 1, g(n) = n³    | f(n) is strictly below g(n) asymptotically. |
| **Big-Omega**| f(n) ≥ c * g(n) for large n, for some constant c > 0.                      | f(n) = 3n² + 2n + 1, g(n) = n     | f(n) is above or equal to g(n) asymptotically. |
| **Small-omega**| f(n) > c * g(n) for large n, for all constants c > 0.                   | f(n) = 3n² + 2n + 1, g(n) = n     | f(n) is strictly above g(n) asymptotically. |
| **Theta**    | c₁ * g(n) ≤ f(n) ≤ c₂ * g(n) for large n, for constants c₁, c₂ > 0.       | f(n) = 3n² + 2n + 1, g(n) = n²    | f(n) grows tightly around g(n) asymptotically. |
