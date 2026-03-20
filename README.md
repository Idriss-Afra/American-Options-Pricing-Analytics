# American Options Pricing Analytics

A quantitative finance repository focused on pricing **American options** through several complementary numerical and analytical approaches.

This project develops three pricing frameworks for American-style options: the **Binomial model**, the **Barone-Adesi & Whaley approximation**, and the **Least-Squares Monte Carlo (LSMC) method**.

---

## Repository Structure

```text
American-Options-Pricing-Analytics/
├── American Options Pricing Analytics.ipynb
├── Barone-Adesi-Whaley 1987.pdf
└── Longstaff-Schwartz Least-Squares MC Approach.pdf
```

---

## Project Overview

This notebook focuses on the pricing of **American options**, where the holder can exercise the contract before maturity and the valuation must therefore account for the **early-exercise feature**. The project compares three standard approaches with different trade-offs in terms of **accuracy**, **speed**, and **implementation complexity**.

The first framework is the **Binomial model**, which prices the option by simulating a recombining tree for the underlying asset and applying **backward induction** to compare continuation value with immediate exercise value at each node. The notebook explicitly distinguishes the European and American recursions and notes that the accuracy improves with the number of time steps, at the cost of higher computation time.

The second framework is the **Barone-Adesi & Whaley 1987 (BAW) approximation**, which estimates the **early-exercise premium** through an analytical adjustment around the **optimal exercise frontier**. In this implementation, the optimal spot boundary is obtained numerically through a **bisection method**, and the repository includes the original reference paper used for the methodology.

The third framework is the **Least-Squares Monte Carlo method**, referenced in the repository through the **Longstaff-Schwartz** paper, and complements the tree-based and approximation-based approaches with a simulation framework adapted to American-style exercise problems.

---

## Documentation

The repository includes two reference documents:

* `Barone-Adesi-Whaley 1987.pdf`
* `Longstaff-Schwartz Least-Squares MC Approach.pdf`

---

## Example Output

```text
Input Data :  {'Contract Size': 100.0, 'Spot Price': 120.0, 'Maturity': 1.0, 'ATM Implied Volatility': 0.35, 'ZC Rate': 0.038, 'Dividend Yield': 0.015}
```

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/37141e11-4d24-4789-b509-9b8d25aeda52" />

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/d3a52fd3-1907-49cd-ad09-e46644811e39" />

---

## Best use case

Use this notebook when working with **American-style options** and comparing **tree-based**, **analytical approximation**, and **Monte Carlo** pricing approaches.

---

## How to Use

Clone the repository:

```bash
git clone https://github.com/Idriss-Afra/American-Options-Pricing-Analytics.git
cd American-Options-Pricing-Analytics
jupyter notebook
```

Then open:

* `American Options Pricing Analytics.ipynb`

---

## Author

**Idriss Afra**
