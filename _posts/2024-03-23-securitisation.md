---
layout: post
title: ESBies/EJBies
date: 2024-03-23 11:12:00
description: Securitization of EU sovereign debt 
tags: Sovereign Bond-Backed Securities (SBBS)
categories: post
related_posts: true
---
   <span style="font-size:0.5em;">
 
   |country |PD | LGD | EAD | $$\rho$$ | $$\rho$$ | $$\rho$$ | $$w_n$$|
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
</span>  
[Source: Author's own based on Brunnermeier(2017) Table 1.]

PD: probability of default; LGD: loss given default;$$\rho$$: correlation of $$B_{n}$$ with common factor; $$w_n$$ weight of country's sovereign bonds in underlying portfolio. 

Cumulative expected tranche loss (as % of total expected loss) - Student t copula
  
|Correlation ($$\rho$$)          | 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% |
 Subordination  | 10/90 |10/90 | 10/90 | |20/80 | 20/80 | 20/80 |
  Junior | 0.437593 | 0.4433023 | 0.4008345 |       | 0.7461881 | 0.7170992 | 0.8166356 |
   Senior | 1.0000000 | 1.0000000 | 1.0000000 |       | 1.0000000 | 1.0000000 | 1.0000000 |
          |       |       |       |       |       |       |  | 
Correlation ($$\rho$$) | 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% | 
Subordination |30/70 | 30/70 | 30/70 |       | 40/60 | 40/60 | 40/60 |
   Junior | 0.808988 | 0.8029003 | 0.8290505 |       | 0.8168696 | 0.8192056 | 0.8308591 |
    Senior | 1.0000000 | 1.0000000 | 1.0000000 |       | 1.0000000 | 1.0000000 | 1.0000000 |
             |       |       |       |       |       |       |  | 
Correlation ($$\rho$$)| 30%  | 50%  | 70%  |       | 30%  | 50%  | 70% |
 Subordination| 50/50 | 50/50 |50/50 |       | iTRAXX | iTRAXX | iTRAXX | 
 Junior | 0.820388 | 0.8276687 | 0.832575 | 0%-3% | 0.0905288 | 0.1473061 | 0.0011647 |
 Senior | 1.0000000 | 1.0000000 | 1.0000000 | 3%-6% | 0.2782576 | 0.3060663 | 0.1780716 |
          |       |       |       | 6%-9% | 0.3984941 | 0.4053905 | 0.3478753 |
          |       |       |       | 9%-12% | 0.5106444 | 0.4995052 | 0.5067522 |
          |       |       |       | 12%-22% | 0.7680178 | 0.73692 | 0.8246559 |
          |       |       |       | 22%-100% | 1.0000000 | 1.0000000 | 1.0000000 |

The table shows the values of $$(E[L]-E[(L-K)^{+}])/E[L]$$, for $$K= 10\%, 20\%,..,100\%$$. Simulations based on probability of default given by PD in Table 1. This table reports expectations of loss from 0 to the upper attachment bound and normalized to the expected loss.	

