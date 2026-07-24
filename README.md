This project constructs an optimized quantitative portfolio framework by applying Random Matrix Theory
to S&P 500 returns. In standard Mean-Variance Optimization, empirical correlation matrices amplify 
statistical noise, causing severe portfolio weight concentration and poor out of sample performance. 
By applying the Marchenko–Pastur distribution, we isolate genuine market signals from pure random noise 
to create a denoised correlation matrix.

Using the cleaned matrix, we perform Maximum Sharpe Ratio optimization under long only constraints using 
SciPy's SLSQP algorithm. Backtesting on unseen out of sample data demonstrates that RMT denoising prevents 
overfitting, lowers weight instability, and yields a superior risk adjusted return compared to uncleaned 
sample covariance models.
