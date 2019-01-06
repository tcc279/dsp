[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> The distribution is uniform

Code:

import numpy as np  
import nsfg  
import first  
import thinkstats2  
import thinkplot  

rand = np.random.random(1000)  
pmf = thinkstats2.Pmf(rand)  
thinkplot.Pmf(pmf, linewidth=0.1)  
thinkplot.Config(xlabel='Random number', ylabel = 'PMF')  
  
cdf = thinkstats2.Cdf(rand)  
thinkplot.Cdf(cdf)  
thinkplot.Config(xlabel= 'Random number', ylabel='CDF')  
