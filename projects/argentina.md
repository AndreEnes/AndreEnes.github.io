---
layout: default
title: Projects
nav_order: 6
---

[Back](/projects.md)

## ML Regression Toolkit (Internship)

This project was developed to solve generic regression problems by finding optimal input parameters for a desired target output using machine learning. It employed the XGBoost library's XGBRegressor for predictions, with hyperparameter tuning handled by Hyperopt, and feature optimization performed using simulated annealing via SciPy’s dual_annealing.

The app featured a user-friendly Streamlit interface, though the machine learning logic was modularized to support integration with other frontends. Users could train models on custom datasets, make predictions from new inputs, and find optimal parameter configurations to approach a target output. The system supported both continuous and discrete variables and allowed detailed model explanation using SHAP values.

A key functionality included incremental model retraining, which significantly reduced computational overhead. Additionally, project configurations were saved using JSON templates for persistent and repeatable workflows. Feature importance was visualized through SHAP beeswarm plots, offering intuitive insights into the model’s decision-making process.

While the toolkit was designed with extensibility in mind, further improvements were identified, such as better discrete optimization via mixed-integer programming, more advanced SHAP plots, and real-time convergence visualization during optimization.

Take a look at the project in the [repo](https://github.com/AndreEnes/argentina-opt).

![argentina](/images/projects/argentina/screenshot.png)

### Tech Explored

- Regression Problems
- Streamlit
- Gradient Assisted Boost Trees
- Hyperparameter Optimization
- Simulated Annealing
- SHAP
- Data Processing

### Highlights

- This internship was right after I had my Machine Learning class, so I got to work on a real project with it right away.
- 1st experience in a "work environment" where I got to participate in academic research.
- The objective of the project was very palpable, so it was great to see improvements daily.
- Streamlit is awesome!

### Lowlights

- Pre ChatGPT days made setting up Python packages a bit messy, since I had little to no guidance on how to properly use all the tools to make software development more reliable.
- The code was quite messy. I don't want to look at it again.
- Streamlit is great, but for bigger projects, it becomes hard to deal with.
- I'm not sure if anyone used it.

### Lessons Learned

- Write code with how to test it in mind.
- Google Colab was a killer idea.
- Put headphones on with no music to listen to office drama. It might help with sleepy 2 o'clocks.
