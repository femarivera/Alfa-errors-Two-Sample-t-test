R simulations for the understanding of the alfa-errors (error of the first kind) in a two sample t-test accounting for different sample sizes.

The code runs a series of simulations, each of one performs a defined number of t-tests for the mean of two samples of size n with the same 
underlying probability distribution (a normal distribution in this case). The simulation is runned for the specified sampled sizes indicated 
in the vector `sample_sizes`. The output consists on boxplots plotting the ratio of significant tests over the total performed tests for each simulation

Please input the parameters for the simulation. `sample_sizes` is a vector containing the desired sizes of the samples with which the t-tests 
are to be performed. The simulation is runned for each sample size at a time. `sign_level` is the arbitrarily defined significance level for 
the t-test, it is used to defined which tests are significant or not, according to their p-values. `total_simulations` contain the number of 
simulations, in each simulation, a series of t-tests is performed, each t-test is performed over two samples of the same size randomly withdrawn 
from a normal distribution with an internally defined mean and standard deviation using `rnorm()`. The t-tests are performed several times per 
simulation (`tests__per_simulation`), just by sub-setting a different random sample from the same distribution each time, so that a percentage 
of significant and not significant tests can be calculated. The parameters of the distribution are the same within a simulation, but they change 
among simulations. At the end, for a given sample size, a boxplot with the alfa-errors is plotted, along with the predefined significance level.

