[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 34.2% percent of men could apply to be a Blue man

Code:

import scipy.stats
mu = 178
sigma = 7.7
z = scipy.stats.norm(loc=mu, scale=sigma)
low = z.cdf(177.8)
high = z.cdf(185.4)
low
high
amt = high - low
amt
