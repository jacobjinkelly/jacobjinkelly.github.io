---
layout:       post
title:        A More Detailed Look at Policy Gradient
summary:      Theoretical results and improvements to the policy gradient algorithm to make it work in practice.
categories:   
---

In a [previous post]({{ site.url}}/2018/06/25/an-exploration-of-some-simple-rl-algorithms/)
I briefly explored why in reinforcement learning we might optimize our policy
(instead of learning the most valuable states), and why we might have a
stochastic policy. In this post I want to explore in much more detail the
policy gradient algorithm. In particular, I want to look at a few nice properties
of policy gradient, and how to make it work in practice.
