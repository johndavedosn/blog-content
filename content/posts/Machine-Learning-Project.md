+++
date = '2026-01-15T20:36:36+01:00'
draft = false
title = 'Machine Learning Project.'
+++

I am quite fairly interested in machine learning and deep learning, while I really suck at the latter and love the former more. Both of them are very cool in my eyes. Such a beautiful mix of math, logic, and programming.

I've worked on many projects in both fields. I made CNNs that were supposed to distinguish between squares and circles, cats and dogs just to name a few. Well, these ones specifically failed miserably to do their job.

Today. I was somewhat bored and took the bad decision to work on an ML project instead of studying for my math exam tomorrow (it's gonna be fine, trust me :D). I searched in Kaggle for datasets or really anything to do and found a DS that caught my attention.

[Exam Score Prediction Dataset](https://www.kaggle.com/datasets/kundanbedmutha/exam-score-prediction-dataset) provides a lot of coverage data for many factors of student life, including sleep, study hours and methods, exam grades and more.

"What if I made an ML model that predicts exam scores?" is a silly question, but boredom embraces silliness. So naturally I downloaded the DS and installed ``sci-kit-learn`` to start cooking, or baking, I don't know.

First off. I wanted to do some feature analysis in order to figure out which features of the DS actually mattered, because I've learnt the hard way that throwing everything at the model and praying that it figures things out on its own is not a wise course of action, so to say.

I started playing with some methods for feature analysis and settled on three main methods:

- **Numerical correlation:** The simplest kind of correlation analysis. I'm pretty sure it is taught in advanced statistics and it works out very well for linear data.
- **Mutual Information (MI):** This method shows us essentially how much uncertainty do we eliminate by including a certain feature. It's very good for non-linear data (apparently) and works well with categorical features, which is good because a lot of the columns in the DS weren't numbers.
- **Permutation Importance:** This is the most important and somewhat deal-breaker method. It actually finds out whether your model is going to be greatly inaccurate if a certain feature is included or not. I relied on it a lot during my analysis.

I would lie if I said that all three methods were equally as meaningful to me, and that's probably wrong. But I mainly relied on Permutation Importance to figure out what feature to include and what to leave out. Others were...complementary to say the least.

I tried out with a lot of features from the DS and came out with a mildly non-shocking conclusion:

Study hours, facility rating, sleep quality and attendance are the most influential factors on exam scores. Other factors' impact is either too small to worry about or completely nonexistent (like age and gender).

Fun fact. I managed to actually get a numerical version of this conclusion which would actually allow us to form something close to a mathematical formula for the best exam score!

While not an accurate prediction equation for exam scores. It's still pretty interesting to check out.

``sci-kit-learn`` provides a way to see the actual weights the model puts for all the features, which then you can use to create a weighted-sum equation.

Study hours are weighted at 5.88. Meaning, each hour of studying adds roughly ~5.88 points to your score.

Good sleep is at 4.52 and bad sleep is at -4.79. So sleep good, folks!

This is the one that surprised me the most. Bad facilities ratings are weighted at a whopping **-7.81**! which means that studying in a bad school deducts roughly eight points from your exam score. WOW!

Even medium facility ratings are at -3.75. Unbelievable. (Unless I did something wrong, this is literally what the code outputs).

Sleeps hours are at 1.43. So each hour of good sleep you get increases your score.

Attendance is at 0.34. not bad.

So the equation to the best exam score in English become: 

"Study more, get good sleep, attend your classes and don't go to a shitty college".

Now, a lot of people would argue that studying in a good manner counts for more than "studying more", and I agree. But at least for the scope of the DS, **study methods had no impact whatsoever on the exam score**.

And it kinda makes sense. After all, if you study in a good method but for little time, you're still going to fail. Trust the science xD.

I then created the actual predictor. Firstly I used a ``RandomForestRegressor`` which is essentially a very fancy nonlinear regression model. The model was really bad and couldn't go under 9 in MAE and over 0.65 in R².

I kept adding and removing features but nothing changed. Then Gemini suggested that maybe the data was linear and I had to use ``LinearRegression`` instead. Sure enough, the metrics went up instantly.

The metrics of the model are currently: 
```
R² score: 0.699634274396406 
MAE: 8.342877921614456
```

Which is actually very good for a model that predicts human-related stuff. We homo-sapiens are just too weird and random to be fully-predictable by math.

It is now in its final state. It can predict - with a decent level of accuracy - student exam scores based on the factors specified earlier.

Well, fellers. We all know that no silly mathematical model can predict our exam scores. And that there's always that ONE GUY in your class that will outperform everyone without even trying. Or vice versa.

This was just a small analysis and prediction project I worked on and it actually taught me a lot about statistics and ML generally. And also, I now know that math can explain everything, even if with slight inaccuracy.