# Understanding Google's PageRank: The Linear Algebra Behind It

Homework for **Computational Linear Algebra** (MSc Data Science and Engineering, Politecnico di Torino course).
Authors: Silva Bashllari and Baharak Qaderi.

## What this is

Worked solutions to the 17 exercises in Kurt Bryan and Tanya Leise's paper [googleFinalVersionFixed.pdf]

PageRank ranks web pages by the eigenvector of a column-stochastic link matrix associated with eigenvalue 1. The exercises explore when that ranking is well defined and how to compute it.

## Topics covered

- **Eigenvector formulation:** ranking pages by solving Ax = x, and how rankings change when pages and links are added
- **Disconnected subwebs:** showing that the eigenspace for eigenvalue 1 has dimension equal to the number of subwebs, so the ranking is not unique
- **Dangling nodes:** pages with no outgoing links, and the Perron eigenvector of the resulting substochastic matrix
- **The modified matrix** M = (1 − m)A + mS (with m = 0.15), which guarantees a unique, positive ranking vector
- **Power method:** convergence of Mᵏx₀ to the ranking vector, and how the second-largest eigenvalue |λ₂| sets the convergence rate
- **Choosing m:** the trade-off between faster convergence and staying faithful to the web's link structure

## Files

- `BashllariQaderi_UnderstandingGooglesPageRank.pdf`: written solutions, including proofs and derivations
- `BashllariQaderiPageRank.ipynb`: numerical exercises in Python (NumPy, SciPy), including eigenvector computations and power-method convergence

## License

Our solutions and code are licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).
The exercises themselves are from Bryan and Leise (2006) and remain under their original copyright.
