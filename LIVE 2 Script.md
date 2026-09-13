# LIVE 2 Script

Part 4 is the heavy tail evaluation and calculation of 0.99-quantile of the loss.

## [Next Page]

The loss is defined by minus log return throughout this part.

First calculate the 99 percentile according to Gaussian and Empirical Estimator.  For Gaussian estimator, fit a Gaussian distribution with the same mean and std, and get quantile accordingly. For empirical estimator, calculate the quantile of the data directly.

## [Next Page]

Second is the POT estimator. Step 1, we should verify the linearity of the mean excess over different thresholds. The sample mean excess plot is over right. We can see that before 0.01 there is some kink. For thresholds over 0.01, the sample mean excess is roughly linear with a clear upward thrend, despite some volatility and outliers.

## [Next Page]

Step 2 is to fit the excess with a general Pareto model using different thresholds. Assign thresholds from 0.01 to 0.08 to fit 8 GPD models and plot the empirical distribution vs fitted distribution plot, we get **this**. It turns out that the goodness of fit is decent for thresholds around 0.01 and 0.04. Considering the abundance of data, we chose threshold around 0.01. Then assign thresholds from 0.01 to 0.03, we found that 0.012 shows best goodness of fit.

## [Next Page]

So the threshold is 0.012, and the empirical vs fitted distribution plot is over right.

## [Next Page]

Then let's look at the hill estimator. There is a hyperparameter k, which is how many order statistics should we choose to calculate alpha. Here is the hill plot. According to an essay called "How to make a hill plot", we should choose a stable area. For k smaller than 200, alpha fluctuates greatly. There is a rather stable area around k=650. 

## [Next Page]

Take a closer look at k=5 to 800. The stable area is clearer. We choose k=650.

## [Next Page]

So now we can calculate all the percentiles, the result is. The plot shows the loss and the percentiles.

## [Next Page]

So, is the 99% loss for Yangtze Power large? We consider make some comparisons.

Firstly let's compare with Gaussian random loss. However we can see that data gererated from Gaussian distribution does not appear to have a similar pattern, which align with our observation in previous parts.

## [Next Page]

Then let's compare with the Wind Public Electricity Index of the same period. The Specs of POT estimation is shown hear, and we choose 0.012 as threshold.

## [Next Page]

Here is the hill plots, we choose k = 300.

## [Next Page]

Then we get the estimations.

## [Next Page]

Then let's compare with the CHI300 of the same period. The Specs of POT estimation is shown hear, and we choose 0.012 as threshold.

## [Next Page]

Here is the hill plots, we choose k = 300.

## [Next Page]

Then we get the estimations.

## [Next Page]

By putting them together, we can see that Yangtze Power has the smallest estimated extreme loss, showing its relatively stable performance.

