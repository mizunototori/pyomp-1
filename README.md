PyOMP Usage Documentation
=========================

### Usage: 

![Sample](https://raw.github.com/sathyamvellal/pyomp/images/sample.png)
 
Import PyOMP module  
`from omp import Omp`

From this point onwards, till the end, a block of code refers to a function with the code inside it. This function shall not take any arguments unless its explicitly specified.  
Use the parallel directive to start a parallel block.  
`@Parallel({"noThreads":4}`

To parallelize a for loop, use the for directive. The function on which this directive (or decorator) is applied takes a list as an arugment, and the for loop must iterate through this  
`@For(List)`

There is also ssupport for a single block and task blocks within  
`@Single`
`@Task`

Sections are created in the same way. With an outer block decorated with "sections" and containing blocks of "section"s within  
`@Sections`
`@Section` 

A sample file is made available. Check [sample.py][1]

### Results 

Benchmarks of a matrix-matrix show that the performance is twice as better. (Lower is better).
![Benchmark](https://raw.github.com/sathyamvellal/pyomp/images/snapshot61.png)

[1]: http://github.com/sathyamvellal/pyomp/tree/master/sample.py