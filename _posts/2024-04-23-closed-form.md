---
layout: post
title: Bond price between coupon payments  
date: 2024-04-23 11:12:00
description: Pricing bonds between coupon payments
tags: Closed-form fomula, bond pricing
categories: post
related_posts: true
---
Gottschalk (2018) presents a simple closed-form formula for bond pricing between coupon payments that derives from first principles and is theoretically correct. The results are more general than the current framework, and encompass the conventional formula for pricing  bonds at coupon dates as a special case.

Let $y\in \mathbb{R}$, let $M, i, w \in \mathbb{R}_{++}$, and let $N\in \mathbb{N}$, then the fair price of a coupon bond between coupon payments is

\begin{equation}
P=q^{w}\left(M\,i\,\frac{1-q^{N+1}}{1-q}+M\,q^{N}\right)\label{tbasic}
\end{equation}

Proof

Let $q\equiv \frac{1}{(1+y)}$, then,

\begin{equation}
P=q^{w}\left(M\,i\sum_{t=0}^{N} q^{t}+M\, q^{N}\right)\label{treasury1}
\end{equation} 

The sum can be expanded to

\begin{equation}
S=q^{0}+q^{1}+q^{2}+...+q^{N}\label{tsum1a}
\end{equation}

Multiplying both sides of (\ref{tsum1a}) by $q$,

\begin{equation}
qS=q^{1}+q^{2}+...+q^{N}+q^{N+1}\label{tsum1b}
\end{equation}

and subtracting (\ref{tsum1b}) from (\ref{tsum1a}), we find

\begin{equation}
S=\frac{1-q^{N+1}}{1-q}\label{tsum1d}
\end{equation}

Substituting (\ref{tsum1d}) into (\ref{treasury1}) yields (\ref{tbasic}).
\end{proof}
                                                                        
## References

Gottschalk, S. (2018). A closed-form formula for pricing bonds between coupon payments. Mathematical Finance Letters. 2018, pp. 1-16.
<a href="https://scik.org/index.php/mfl/article/view/3650/1793">https://scik.org/index.php/mfl/article/view/3650/1793</a>
<a href="https://repository.mdx.ac.uk/item/87qzz">https://scik.org/index.php/mfl/article/view/3650/1793</a>
