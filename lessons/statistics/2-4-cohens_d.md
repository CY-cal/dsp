[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 
Labeling the first and the other babies 

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
= -0.088672927072602

CohenEffectSize(firsts.prglngth,others.prglngth)
=  0.028879044654449883
 
For the babies' weight, the difference of mean in Cohen's d is less than 0.2, which indicates the result is trivial.
Same to the babies pregnant length, the difference of mean in Cohen's d is less than 0.2, which indicates the result is trivial again.

Therefore, the mean in weight, and pregnancy length between the first babies and the other babies, have no significant difference in general. 
