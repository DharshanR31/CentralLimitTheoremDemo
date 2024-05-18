# CentralLimitTheoremDemo

Central Limit Theorem Demo
This project demonstrates the principles of the Central Limit Theorem by sampling a given input distribution 1000 times with a user specified sample size.

## Requirements
If plotting is enabled, [Matplotlib](https://matplotlib.org/) and [Seaborn](http://seaborn.pydata.org/) are required.

## Usage
The central_limit_theorem_demo.py file contains a CentralLimitTheorem class. It can be instantiated with a distribution in the form of a list.

import central_limit_theorem_demo as clt

some_distribution = create_distribution(...)
cltDemo = clt.CentralLimitTheorem(some_distribution)
The demo can be run via the run_sample_demo method on CentralLimitTheoremDemo. This method takes a sample size N, a plotting flag plot, and an optional num_bins parameter describing the number of bins to use when plotting the demo output.

## Example
A full example might look something like this.

import central_limit_theorem_demo as clt

def create_uniform_sample_distribution():
    return range(100)

def run():
    sampleDistribution = create_uniform_sample_distribution()
        
    # Plot the original population distribution
    clt.plot_distribution(sampleDistribution, "Population Distribution", 0, 100, 20)
        
    # Plot a sampling distribution for values of N = 2, 3, 10, and 30
    cltDemo = clt.CentralLimitTheoremDemo(sampleDistribution)
    n_vals = [2, 3, 10, 30]
    for N in n_vals:
        cltDemo.run_sample_demo(N = N, plot = True, num_bins = 40)
This produces the following output images.

![uniform_dist](https://github.com/DharshanR31/CentralLimitTheoremDemo/assets/109989995/847100dc-c29f-408f-b322-6a36cacf9d19)

![uniform_n_2](https://github.com/DharshanR31/CentralLimitTheoremDemo/assets/109989995/b0735d51-739e-44af-980a-8407909ab4cc)

![uniform_n_3](https://github.com/DharshanR31/CentralLimitTheoremDemo/assets/109989995/32c8b695-928d-484b-9f8a-840753f5558f)

![uniform_n_10](https://github.com/DharshanR31/CentralLimitTheoremDemo/assets/109989995/ba72c655-c44d-4e5c-8696-4cdf4f1d450e)

![uniform_n_30](https://github.com/DharshanR31/CentralLimitTheoremDemo/assets/109989995/11a1d78e-83ea-4990-8d7d-3bf4ea4158aa)
