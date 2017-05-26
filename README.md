# BIF_Generator
[![Build Status](https://travis-ci.org/sfu-cl-lab/BIF_Generator.svg?branch=master)](https://travis-ci.org/sfu-cl-lab/BIF_Generator)       
Code for Exporting a learned First-Order Bayesian Network to a Bayesian Network in BIF format. 

Input: 

+ A relational database
+ A learned Bayesian network (using [FactorBase](https://github.com/sfu-cl-lab/FactorBase)).

Output: An .xml file in BIF format.

## How to Use 

1. First import data into your database and run [FactorBase](https://github.com/sfu-cl-lab/FactorBase). 
2. Set up a configuration file as for running [FactorBase](https://github.com/sfu-cl-lab/FactorBase). If you use BIF_Generator after Factorbase, you can just keep the same configuration file.
3. Export the learned BN by running `java -jar BIF_Generator.jar`.
4. The output file is named `Bif_YOURDATABASENAME.xml`    

  
## Examine Bayesian Network in GUI (Visualization)    
We have tested the BIF_Generator with the AIspace tool from UBC.  
[Download tool (.jar format)](http://www.aispace.org/bayes/version5.1.10/bayes.jar)    
[Download tool (.exe format)](http://www.aispace.org/bayes/version5.1.10/bayes.exe)    

  
### Compile & Run (Alternative way to run BIF_Generator)    
+ Go into `cfg` folder and modify `subsetctcomputation.cfg` to make it identical to the config file you use to run FactorBase.    
+ `javac -cp ".:./lib/*" BIF_Generator.java`  
+ `java -cp ".:./lib/*" BIF_Generator`  
