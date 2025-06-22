---
layout: post
title: Introduction to Causal Inference
---

## The Potential Outcomes Framework

The potential outcomes framework offers an elegant and tractable way to talk about 
counterfactuals in the language of random variables (Rubin, 1974). This framework 
connects questions of causality to questions of statistics, providing a rigorous 
foundation for causal analysis.

In the potential outcomes framework, we use specific notation to represent different 
treatment scenarios

- Let $$Y_{i,t}(0,0)$$ denote unit $$i$$'s potential outcome at time $$t$$ if it 
  remained untreated in both periods.

- Let $$Y_{i,t}(0,1)$$ denote unit $$i$$'s potential outcome at time $$t$$ if 
  untreated in the first period but exposed to the treatment by the second period.

### The Fundamental Problem of Causal Inference

In practice, we face a fundamental limitation: we never observe both $$Y_{i,t}(1)$$ 
and $$Y_{i,t}(0)$$ for the same unit at the same time. This is known as the 
fundamental problem of causal inference.

Instead, the data we observe, $$Y_{i,t}$$, consists of
- Treated outcomes $$Y_{i,t}(1)$$ for treated units
- Untreated outcomes $$Y_{i,t}(0)$$ for untreated units

We can express this relationship as

$$
Y_{i,t} = (1 - D_i) Y_{i,t}(0) + D_i Y_{i,t}(1),
$$

where $$D_i$$ is the treatment indicator that equals 1 if unit $$i$$ is treated 
and 0 otherwise.