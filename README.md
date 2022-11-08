# Quantum Dot Optimization #

## Required Packages ##
The notebook was tested with python 3.8.10
The current notebook requires the following packages and is tested on the 
reported versions

tensorflow==2.8.0
scipy==1.8.1
scikit-learn==1.0.2
pandas==1.4.0
numpy==1.22.3
keras==2.8.0
GPy==1.10.0

## How to use ##
Run the cells sequentially. 
The final one, under the Heading RUN BO will produce
one suggestion for the ratios of the precursor solutions for each of the nanoplatelet
numbers of interest. The number of nanoplatelets are defined by changing the variable : nano. 

Additionally, one can specify if the suggestions should give priority to precurson ratios with  peak positions closer to the middle of the range specified for the specific nanoplatelet number. 
This is done with the variable middle const. It can take the values 0, where no priority is given to suggestions closer to the center of the peak range, and 1, where a priority is given.


Further, the value of the variable lower_bound signifies the minimum value a precursor ratio can take. 

the variable "method" indicates which acquisition function to be used. Available options are:
expected improvement : "pe"
probability of improvement : "pi"
upper confidence bound : "ucb"


the variable tradeoff  denotes the tradeoff between exploration and exploitation for the acquisition functions that this is applicable.
