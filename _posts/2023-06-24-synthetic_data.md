---
layout: post
title:  Synthetic data in finance
date:   2023-06-24 16:40:16
description: Applications of agent-based model to create personal data
tags: FinTech 
categories: post
---
The 2nd <a href="https://www.eftconference.business-school.ed.ac.uk/">Conference on the Economics of Financial Technology</a> gathered more than 100 academics researching on FinTech and AI applications to finance. There were also a couple of industry applications presented. One of them, Smart Data Foundry, builds on the agent-based models to create synthetic data. The presentation showed how synthetic data can be used by banks to simulate the behaviour of clients without using actual personal data, which can be problematic due to confidentiality requirements or disclosure risks. 

#### What are synthetic data?

Synthetic data are computationally generated to replicate the same characteristics of real data: people, firms, events, interatcions between firms and people. The main difference is that part of these characteristics, or all of them, are artificial. Synthetic data are useful to

<ul>
    <li>enable applications that would not be possible with real data</li>
    <li>increase existing datasets to allow the analysis of new scenarios, which cannot be simulated with existing data</li>
    <li>run simulations without putting at risk the data of real peoples</li>
    <li>simulate events for which there are no data, e.g., impact of Brexit before Brexit</li>
</ul>

#### How are synthetic data generated?

Two main approaches were presented: 

<ul>
    <li>Agent-based modelling (ABM): was developed in economics in the 1990s as agent-based computational economics (ACE). An "agent" is any entity capable of affecting the trajectory of outcomes for a system, such as decision-making entities (e.g., "humans") or physical phenomena with no cognitive function (e.g., "weather"). One of the main characteristics of ABM is the large number of heterogeneous agents. This strongly contrasts with mainstream economics models which are based on the representative consumer, the representative firm, or the representative central planner.</li>
    <li>Learning-based synthesis: is based on machine learning and machine training on real data. A model is created and trained on real data to learn the patterns in the dataset. The learned patterns are then used to generate synthetic data with the same characteristics and patterns of the real data.</li>
    
</ul>

#### Why synthetic data?

The concept of synthetic data is puzzling for academics, who aim to produce research that leads to accurate predictions, even though economic models are abstract and rely on simplifying assumptions (e.g. representative consumer). Using real data is thus fundamental for research economists. Some colleagues were disturbed by the very concept of synthetic data, which they interpreted as "fake" data. I had a conversation with the Smart Data Foundry's Principal Data Scientist Paola Arce, and asked why not use anonymised real data instead of synthetic data. Paola explained that anonymised data may be made available to academics but never to businesses. Even regulators such as the Financial Conduct Authority would have difficulty accessing personal data from firms outside their remit (e.g. data from the Payment Systems Regulator). Synthetic data fill this gap and allow businesses and regulators to analyse consumer behaviour. 

<hr>

The presentation was very enlightening and it is good to see real life applications of agent-based models. Hopefully, these models will become more mainstream in economics and finance syllabi. 

#### References

Smart Foundry White Paper: <a href="https://smartdatafoundry.com/news/white-paper-comparing-synthetic-data-approaches-simulation-learning-based-synthesis">https://smartdatafoundry.com/news/white-paper-comparing-synthetic-data-approaches-simulation-learning-based-synthesis</a>

