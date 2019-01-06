[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> Unbiased PMF mean: 1.024 
   Biased PMF mean: 2.403

Code: 

import numpy as np  
import nsfg  
import thinkstats2  
import pandas  

resp = nsfg.ReadFemResp()  
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')  
thinkplot.Pmf(pmf)  
thinkplot.Config(xlabel='Number of Children', ylabel = 'PMF')  

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)  
    for x, p in pmf.Items():  
        new_pmf.Mult(x,x)  
    new_pmf.Normalize()  
    return new_pmf  

biased_pmf = BiasPmf(pmf, label = 'observed')  
thinkplot.PrePlot(2)  
thinkplot.Pmfs([pmf, biased_pmf])  
thinkplot.Show(xlabel= 'Number of Children' , ylabel = 'PMF')  
  
  
pmf.Mean()  
biased_pmf.Mean()  
