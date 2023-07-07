---
layout: post
title: CAPM as discount rate
date: 2023-07-06 11:12:00
description: Death to CAPM 
tags: CAPM, volatility, asset pricing
categories: post
related_posts: true
---
Very strong words in the <a href="https://www.ft.com/content/efe30c0c-c239-4528-a643-0a888b6c897d">Financial Times!</a>. 
The article refers to the use of CAPM's expected return of a stock as a discount factor in corporate valuation models. 

\begin{equation}
\label{eq:PV}
{\rm PV}_t=\sum_{s\geq1}\frac{E_t\left[{\rm CF}_{t+s}\right]}{\left(1+r\right)^s}
\end{equation}

where $PV_t$ is the present value of the expected cash flows of the project (or asset), $CF_{t+s}$ are the future cash flows, $E_t[]$, the expectation operator, and $r$ the discount rate. This generic model has many applications, e.g., the perpetual dividend model (PV is the stock price), or project valuation.

The discount rate should also be stochastic in model (\ref{eq:PV}), since it is usually based on the CAPM equation
\begin{equation}
\label{eq:PV}  
E_t[R_{it}]= r_f+\beta\left[E_t[R_{mt}-r_f\right]
\end{equation}

where $R_{it}$ is the return of the stock at time $t$, $R_f$ the risk-free rate and $R_{mt}$ the market return. CAPM’s flaw as a predictor of stock prices come from the confusion between risk and volatility! Beta is a measure of volatility, not risk, and the discount rate required for project and stock price valuation should be a measure of risk. The average realized return of high beta securities does not differ much from low beta securities (Frazzini and Pedersen 2014, Hong and Sraer 2016)
Despite all this, CAPM is still commonly used by firms to calculate discount rates (Graham 2022, Jagannathan et al. 2016, Gormsen and Huber 2022).
                                                                        
## References

Frazzini, Andrea, and Lasse Pedersen, 2014, Betting against beta, Journal of Financial Economics 111, 1–2, https://doi.org/10.1016/j.jfineco.2013.10.005. 

Gormsen, Niels Joachim and Huber, Kilian, Equity Factors and Firms’ Perceived Cost of Capital (January 4, 2023). Available at SSRN: https://ssrn.com/abstract=3712699 or http://dx.doi.org/10.2139/ssrn.3712699 

Graham, John, 2022, Corporate finance and reality, Journal of Finance, https://doi.org/10.1111/jofi.13161

Nicolas Hommel, Augustin Landier, David Thesmar (2023) Corporate valuation:An empirical comparison of discounting methods, Working Paper 30898
http://www.nber.org/papers/w30898

Hong, H. and Sraer, D.A. (2016), Speculative Betas. The Journal of Finance, 71: 2095-2144. https://doi.org/10.1111/jofi.12431

Ravi Jagannathan, David A. Matsa, Iwan Meier, Vefa Tarhan(2016) Why do firms use high discount rates?, Journal of Financial Economics, Volume 120, Issue 3,Pages 445-463,
https://doi.org/10.1016/j.jfineco.2016.01.012.

<a href="https://youtu.be/KmQk4zkrdzU">Hear Warren Buffett on beta, volatility and risk</a>  . 

