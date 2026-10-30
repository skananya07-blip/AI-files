## Bayes theorem
# Bayes' Theorem

$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

Where:
* **$P(A|B)$**: **Posterior probability** (Probability of hypothesis $A$ given evidence $B$)
* **$P(B|A)$**: **Likelihood** (Probability of evidence $B$ given hypothesis $A$)
* **$P(A)$**: **Prior probability** (Initial probability of hypothesis $A$)
* **$P(B)$**: **Evidence** (Total probability of evidence $B$)

$P(p_i|m)=\frac{p(m|p_i)p(p_i)}{\sum p(m|p_i)p(p_i)}$
# Supplier Defect Analysis Using Bayes' Theorem

**Supplier A** has the highest probability of being the source of the defective phone. 

Here is the complete step-by-step mathematical breakdown.

## 1. Given Probabilities

Let $A, B, C$ represent the events that a phone is sourced from Supplier A, B, or C respectively. Let $D$ represent the event that a phone is defective.

* **Prior Probabilities (Market Share):**
  * $P(A) = 0.40$
  * $P(B) = 0.35$
  * $P(C) = 0.25$

* **Conditional Probabilities (Defect Rates):**
  * $P(D|A) = 0.03$
  * $P(D|B) = 0.02$
  * $P(D|C) = 0.04$

---

## 2. Total Probability of a Defective Phone $P(D)$

Using the Law of Total Probability, we find the overall probability of selecting a defective phone from the entire inventory:

$$P(D) = [P(A) \cdot P(D|A)] + [P(B) \cdot P(D|B)] + [P(C) \cdot P(D|C)]$$

$$P(D) = (0.40 \cdot 0.03) + (0.35 \cdot 0.02) + (0.25 \cdot 0.04)$$

$$P(D) = 0.012 + 0.007 + 0.010 = \mathbf{0.029}$$

---

## 3. Applying Bayes' Theorem

We now calculate the posterior probability for each supplier to determine which one is most likely responsible for the defect.

### Supplier A
$$P(A|D) = \frac{P(A) \cdot P(D|A)}{P(D)} = \frac{0.012}{0.029} \approx \mathbf{41.38\%}$$

### Supplier B
$$P(B|D) = \frac{P(B) \cdot P(D|B)}{P(D)} = \frac{0.007}{0.029} \approx \mathbf{24.14\%}$$

### Supplier C
$$P(C|D) = \frac{P(C) \cdot P(D|C)}{P(D)} = \frac{0.010}{0.029} \approx \mathbf{34.48\%}$$

---

## Final Conclusion

| Supplier | Share of Supply | Defect Rate | Probability of Sourcing the Defect |
| :---: | :---: | :---: | :---: |
| **Supplier A** | **40%** | **3%** | **41.38% (Highest)** |
| Supplier B | 35% | 2% | 24.14% |
| Supplier C | 25% | 4% | 34.48% |

Even though Supplier C has the highest individual defect rate (4%), **Supplier A is the most likely source of the defective phone** because their high volume of total shipments outweighs the slightly higher defect percentage of Supplier C.
