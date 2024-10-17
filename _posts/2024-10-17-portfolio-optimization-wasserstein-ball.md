---
layout: post
title: "Portfolio Optimization within a Wasserstein Ball"
date: 2024-10-17
---

In this post, I summarize the paper "Portfolio Optimization within a Wasserstein Ball" by Silvana M. Pesenti and Sebastian Jaimungal, and implement the paper in Python code.

Introduction.\\
The widespread use of exchange-traded funds (ETFs) tracking specific indices reflects investors' focus on benchmarks like the S&P 500 or the Dow Jones Industrial Average. However, these benchmarks may not fully align with investors' risk preferences. To adjust, investors may deviate from the benchmarks to better manage downside risk or pursue higher gains while still staying close to the benchmark's terminal wealth. This allows flexibility in aligning investment strategies with personal risk preferences, often captured by distortion risk measures such as the Tail Value-at-Risk (TVaR), a common tool in financial risk management.

This paper addresses investors' concerns about the risk of underperforming a benchmark while seeking to align their terminal wealth with personal risk preferences. Investors may allow their strategies to deviate from the benchmark but remain close, using a copula to define the dependence between their strategy and the benchmark. To measure the deviation between the terminal wealth of their strategy and the benchmark, the Wasserstein distance is applied. Investors aim to balance staying close to the benchmark while optimizing risk-reward profiles using distortion risk measures.

The paper formulates the investor’s portfolio choice as a convex optimization problem over quantile functions. The optimal strategy is derived using an isotonic projection of a combination of the benchmark's terminal wealth, a distortion risk measure, and a stochastic discount factor. Investors’ choices of the Wasserstein distance and copula influence how closely they track the benchmark. When the Wasserstein constraint is removed, the problem reduces to classical portfolio optimization.

The paper contrasts this approach with passive portfolio management, aiming to track the benchmark, and other works focused on model uncertainty, which use the Wasserstein distance in portfolio optimization but do not consider benchmarks. This approach allows for practical portfolio optimization in any market model that can be simulated, providing a more flexible strategy that balances benchmark tracking with personalized risk preferences.


2. Problem Formulation
In this section, the author introduce the market model and develop the investor’s optimisation problem.

2.1. The Market Model

We define the market model on a filtered probability space \(\Omega, P, \mathcal{F} = {\mathcal{F_t}_{t\in[0,T]}}, \mathbb{F}\)

$$
S = (S^1_t, \dots, S^d_t)_{t \geq 0}
$$







Check out the full implementation [here](https://github.com/your-username/wasserstein-portfolio-optimization).

