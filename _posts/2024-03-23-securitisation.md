---
layout: post
title: ESBies/EJBies
date: 2024-03-23 11:12:00
description: Securitization of EU sovereign debt 
tags: Sovereign Bond-Backed Securities (SBBS)
categories: post
related_posts: true
---
## Securitisation of EU sovereign debt

Gottschalk(2022) constructs a structural model of a synthetic CDO where the underlying is a portfolio of government bonds of all the 19 Eurozone countries, and the default correlation structure of portfolio loss is modeled as a Bernoulli mixture. We show that expected tranche losses of CDOs are accurately calculated by saddlepoint approximations. Numerical simulations demonstrate that under correlation structures implying higher probabilities of extreme events, even high levels of subordination cannot shield the senior tranche from default losses.  

## Model
The value of government's fiscal balance can be described by a multi-factor model 

\begin{equation}
D_{n}=\sum_{j}\rho_{n,j}F_j + a_{n}Z_{n}\label{factor1}
\end{equation}

for $$n=1,\ldots,N$$. $$F_j$$, $$j=1,\dots,J$$, are i.i.d. standard Normal distributions, and $$a_n^2+\sum_{j=1}^{J}\rho_{n,j}^2=1$$, with $$\rho_{n,j} \in [0,1]$$. These factors $$\mathbf{F} \in R^J$$ represent global macroeconomic variables that affect all Eurozone countries, e.g., the 2008 Financial Crisis, the 2011-2014 Eurozone Sovereign Debt Crisis, or the 2020 Covid-19 pandemic. $$Z_{n}$$, on the  contrary, is a country-specific, idiosyncratic factor that only affects country $$n$$. Both $$\mathbf{F}$$ and $$Z_n$$ are mutually independent random variables with mean 0 and variance 1. Vasicek (1987) has shown individual defaults are independent of each other given the occurrence of the factor $$\mathbf{F}$$. The probability of individual defaults conditional on $$\mathbf{F}=\mathbf{u}$$, $$p_n(\mathbf{u})$$, is given by

\begin{equation}
P[D_n<K_n|\mathbf{F}=\mathbf{u}]=p_n(\mathbf{u})=P\left[Z_{n}<\frac{K_n-\boldsymbol{\rho^{T} F}}{\sqrt{1-\sum_{j=1}^{J}\rho_{n,j}^2}}\right]=\Phi\left(\frac{K_n-\boldsymbol{\rho^T F}}{\sqrt{1-\sum_{j=1}^{J}\rho_{n,j}^2}}\right)\label{cond1c}
\end{equation}

where $$\Phi$$ is the cumulative Normal distribution, $$\boldsymbol{\rho}\,, \mathbf{F} \in \mathbb{R}^J$$, and $$\mathbf{u} \in \mathbb{R}^J$$, and $$\boldsymbol{\rho}^T$$ is the transpose of $$\boldsymbol{\rho}$$.

Table 1 summarises the simulation inputs, which were taken from Brunnermeier et al.(2017), Rossi (2019), and the European Systemic Risk Board (ESRB, 2018a,b) in order to allow comparison of our results with theirs. Table 1 ranks countries in ascending order of default probability. The country more likely to default is Greece, with a default probability of 95%. Brunnermeier et al.(2017) selected these rates from Deutsche Bank's default probabilities inferred from Credit Default Swaps (CDS) spreads assuming a 40% constant LGD rate. As can be seen from Table 1, this is the LGD assumed for Germany, The Netherlands and Luxembourg.  For other countries, Brunnermeier et al.(2017) calculated analogous default probabilities as those implied by CDS spreads in December 2015. Three levels of correlation with the global factor are considered, 30, 50 and 70 percent. Finally, we calculated other parameters, e.g., portfolio weights, in order to ensure model consistency.

  
   |Country |PD | LGD | EAD | $$\rho_1$$ | $$\rho_2$$ | $$\rho_3$$ | $$w_n$$|
   |:----------------------------------------------------------------------|
   | Germany | 0.05  | 0.4   | 1327816 | 0.3   | 0.5   | 0.7   | 0.2816 |
   | The Netherlands | 0.1   | 0.4   | 388866 | 0.3   | 0.5   | 0.7   | 0.0661 |
   | Luxembourg | 0.1   | 0.4   | 13321 | 0.3   | 0.5   | 0.7   | 0.0019 |
   | Austria | 0.15  | 0.45  | 267570 | 0.3   | 0.5   | 0.7   | 0.03219 |
   | Finland | 0.15  | 0.45  | 128630 | 0.3   | 0.5   | 0.7   | 0.0202 |
   | France | 0.25  | 0.6   | 2105140 | 0.3   | 0.5   | 0.7   | 0.2125 |
   | Belgium | 0.3   | 0.625 | 418295 | 0.3   | 0.5   | 0.7   | 0.03935 |
   | Estonia | 0.35  | 0.625 | 2970  | 0.3   | 0.5   | 0.7   | 0.00035 |
   | Slovakia | 0.35  | 0.7   | 46522 | 0.3   | 0.5   | 0.7   | 0.0066 |
   | Ireland | 0.4   | 0.7   | 214903 | 0.3   | 0.5   | 0.7   | 0.018 |
   | Latvia | 0.5   | 0.75  | 11993 | 0.3   | 0.5   | 0.7   | 0.0017 |
   | Lithuania | 0.5   | 0.75  | 15797 | 0.3   | 0.5   | 0.7   | 0.0025 |
   | Malta | 0.55  | 0.75  | 5924  | 0.3   | 0.5   | 0.7   | 0.0007 |
   | Slovenia | 0.6   | 0.78  | 32771 | 0.3   | 0.5   | 0.7   | 0.00375 |
   | Spain | 0.6   | 0.8   | 1094947 | 0.3   | 0.5   | 0.7   | 0.1077 |
   | Italy | 0.65  | 0.8   | 2355858 | 0.3   | 0.5   | 0.7   | 0.16525 |
   | Portugal | 0.7   | 0.8   | 261426 | 0.3   | 0.5   | 0.7   | 0.0177 |
   | Cyprus | 0.75  | 0.875 | 30348 | 0.3   | 0.5   | 0.7   | 0.0019 |
   | Greece | 0.95  | 0.95  | 348350 | 0.3   | 0.5   | 0.7   | 0.0201 | 
   | average | 0.421053 | 0.663421 |                              |
 
[Table 1. Simulation inputs - Source: Author's own based on Brunnermeier(2017) ]

In Table , PD is the probability of default; LGD the loss given default; $$\rho_i$$ is different values for the correlation of $$D_n$$ with common factor; and $$w_n$$ weight of country's sovereign bonds in underlying portfolio. 

Table 2 shows the values of $$(E[L]-E[(L-K)^{+}])/E[L]$$, for $$K= 10%, 20%,..,100%$$. Simulations based on probability of default given by PD in Table 1. This table reports expectations of loss from 0 to the upper attachment bound and normalized to the expected loss.	

  
|Correlation ($$\rho$$) | 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% |
| Subordination          | 10/90 |10/90 | 10/90 |     |20/80 | 20/80| 20/80 |
| Junior                 | 0.4376 | 0.4433 | 0.4008 | | 0.7463 | 0.7171 | 0.8166 |
| Senior                 | 1.0000 | 1.0000 | 1.0000 | | 1.0000 | 1.0000 | 1.0000 |
|          |       |       |       |       |       |       |  | 
|Correlation ($$\rho$$) | 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% | 
|Subordination |30/70 | 30/70 | 30/70 |       | 40/60 | 40/60 | 40/60 |
|   Junior | 0.8090 | 0.8029 | 0.8291 |       | 0.8169 | 0.8192 | 0.8309 |
|    Senior | 1.0000 | 1.0000 | 1.0000 |       | 1.0000 | 1.0000 | 1.0000 |
|             |       |       |       |       |       |       |  | 
|Correlation ($$\rho$$)| 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% |
| Subordination| 50/50 | 50/50 |50/50 |       | iTRAXX | iTRAXX | iTRAXX | 
| Junior | 0.820388 | 0.8276687 | 0.832575 | 0%-3% | 0.0905288 | 0.1473061 | 0.0011647 |
| Senior | 1.0000 | 1.0000 | 1.0000 | 3%-6% | 0.2783 | 0.3061 | 0.1781 |
|        |       |       |       |           | 6%-9% | 0.39850 | 0.4054 | 0.3479 |
|        |       |       |       |           | 9%-12% | 0.5106 | 0.4995 | 0.5068 |
|        |       |       |       |           |12%-22% | 0.7680 | 0.7369 | 0.8247 |
|        |       |       |       |           |22%-100% | 1.0000 | 1.0000 | 1.0000 |
[Table 2. Cumulative expected tranche loss (as % of total expected loss) - Student t copula]

Table 2 shows the expected tranche losses of the EJBies and ESBies, when 1 million  Monte Carlo simulations of equation (\ref{factor1})  with Student t copula are run. The Student t distribution has heavier tails than the Gaussian distribution, and has long been recognised as more appropriate to capture extreme financial losses. The value of the total expected loss has increased to $$E[L]$$ = 0.17 and the maximum possible loss is $$L_{max}$$ = 66 percent of the underlying portfolio. Table 2 clearly shows that even at a 50/50 subordination level the Senior tranche incurs losses of at least 17% of the total expected portfolio losses ($$\rho=0.3$$). These are the lowest levels of losses of all the subordination schemes. For the 10/90 subordination, the expected losses of the Senior tranche are the highest and reach 60% ($$\rho=0.7$$). For 10/90, $$\rho=0.3$$ and $$\rho=0.5$$,  the expected losses of the Senior tranche are 0.56%. 


## References
Brunnermeier, M., Langfield, S., Pagano, M., Reis, R., Van Nieuwerburgh, S. and Vayanos, D. (2017), ‘ESBies: Safety in the tranches’, Economic Policy 32(90), 175– 219.URL: https://doi.org/10.1093/epolic/eix004

ESRB (2018a), Sovereign bond-backed securities: a feasibility study, Technical report, European Systemic Risk Board High-Level Task Force on Safe Assets. URL: https://www.esrb.europa.eu/pub/task force safe assets/shared/pdf/esrb.report290118 sbbs volume I mainfindings.en.pdf

ESRB (2018b), Sovereign bond-backed securities: technical findings, Technical report, European Systemic Risk Board High-Level Task Force on Safe Assets. URL: https://www.esrb.europa.eu/pub/task force safe assets/shared/pdf/esrb.report290118 sbbs volume II technicalanalysis.en.pdf

Gottschalk, Sylvia (2022a). A Factor Model of Securitisation of Sovereign Debt in the European Union. https://ssrn.com/abstract=4029723.

Rossi, S. (2019), Sovereign debt restructuring and debt mutualisation in the Euro Area: An assessment, Supporting Analyses PE 634.396, European Parliament.

Vasicek, O. (1987), `Probability of loss on loan portfolio', KMV Corporation. http://defaultrisk.com/pp model 60.htm.
