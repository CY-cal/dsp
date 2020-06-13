[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>>(BiasPmf function)

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
    
Use the function to find out the differences between actual distributions and the biased distribution of NUMDKHH 
(How many numbers for each children in their household)
    
    resp = nsfg.ReadFemResp()
    d = resp.numkdhh
    pmf = thinkstats2.Pmf(d, label = 'actual')
    biased_pmf = BiasPmf(pmf, label='observed')
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased_pmf])
    thinkplot.Config(xlabel='Number of Children', ylabel='PMF')
    print('Actual mean', pmf.Mean())
    print('Observed mean', biased_pmf.Mean())
    
    Actual mean 1.024205155043831
    Observed mean 2.461860525971477
    
Because there are a higher possibility for us to reach a child with a larger number of household,
therefore, we have to multiply the number of students who observed that class size
