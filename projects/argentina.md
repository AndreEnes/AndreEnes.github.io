---
layout: default
title: argentina-opt - Machine Learning Optimisation Toolkit
nav_order: 6
---

[Back](../)

## argentina-opt: Machine Learning Optimisation Toolkit

A toolkit for the inverse of a normal regression problem. Instead of asking what output a given set of inputs produces, you give it the output you want and it searches for the input values that get you there.

An XGBoost regressor, tuned with Hyperopt, does the predicting. SciPy's dual_annealing does the searching, and discrete variables are handled by rounding the result to the nearest allowed step. Retraining is incremental, through XGBRegressor's `xgb_model=` argument. SHAP explains what the model is relying on. The interface is Streamlit, but I kept the machine learning in a separate `opt_model.py` so that it did not depend on the UI.

Not everything got finished. Beeswarm is the only SHAP plot implemented, discrete optimisation deserves proper mixed-integer handling, and there is no way to watch the annealing converge while it runs.

Take a look at the project in the [repo](https://github.com/AndreEnes/argentina-opt).

![argentina](/images/projects/argentina/screenshot.png)

### Tech Explored

- Regression Problems
- Streamlit
- Gradient Assisted Boost Trees
- Hyperparameter Optimisation
- Simulated Annealing
- SHAP
- Data Processing and Transformation

### Highlights

- This internship was right after I had my Machine Learning class, so I got to work on a real project with it right away.
- 1st experience in a "work environment" where I got to participate in academic research.
- The objective of the project was very palpable, so it was great to see improvements daily.
- Streamlit is awesome!

### Lowlights

- The pre-ChatGPT days made setting up Python packages a bit messy, since I had little to no guidance on how to properly use all the tools to make software development more reliable.
- The code was quite messy. I don't want to look at it again.
- Streamlit is great, but for bigger projects, it becomes hard to deal with.
- The internship ended before I could find out how it was used.

### Lessons Learned

- Write code with how to test it in mind.
- Google Colab <3.
- Put headphones on with no music to listen to office drama. It might help with sleepy 2 o'clocks.
