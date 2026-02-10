---
title: "Physics-Informed Neural Networks Are Not Magic"
date: 2026-02-06T14:30:00-08:00
link: "https://en.wikipedia.org/wiki/Physics-informed_neural_networks"
tags: ["machine learning", "soil physics"]
---

I keep seeing breathless announcements about PINNs solving problems that couldn't be solved before. And yes, embedding physical laws as constraints in neural network loss functions is genuinely clever. But a PINN that doesn't respect mass conservation is just a fancy curve fitter. The physics has to be right first. *Then* the neural network can help.
