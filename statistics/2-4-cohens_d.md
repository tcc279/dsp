[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> On average, first born children weigh less than other children: the total weight of first borns is 7.2 lbs and the others is 7.3 lbs. Cohen's d for the two groups is 0.088, which is not very large, indicating that the difference in weight between first borns and other babies is small. There is a greater difference beween pregnancy length (Cohen's d = 0.0288) of first and others, but that too is small. 

Code:

import numpy as np
import nsfg
import thinkstats2

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

firsts.prglngth.mean()

others.prglngth.mean()

CohenEffectSize(firsts.prglngth, others.prglngth)

firsts.totalwgt_lb.mean()

others.totalwgt_lb.mean()
