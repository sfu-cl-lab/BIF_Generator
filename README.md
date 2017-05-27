# BIF_Generator
[![Build Status](https://travis-ci.org/sfu-cl-lab/BIF_Generator.svg?branch=master)](https://travis-ci.org/sfu-cl-lab/BIF_Generator)       
Code for Exporting a learned First-Order Bayesian Network to a Bayesian Network in BIF format. 

Input: 

+ A relational database
+ A learned Bayesian network (using [FactorBase](https://github.com/sfu-cl-lab/FactorBase)).

Output: An .xml file in BIF format.

## How to Use 


1. Import data into your database and run [FactorBase](https://github.com/sfu-cl-lab/FactorBase). 

    ***You have already done step 1 if you have been following FactorBase README***

2. Clone the BIF_Generator repository by 

    `git clone https://github.com/sfu-cl-lab/BIF_Generator.git`
  
3. Navigate to `BIF_Generator/cfg` folder and 
    modify the config file `subsetctcomputation.cfg` by copying the same config file content that you used to run FactorBase.  

<!--2. Set up a configuration file as for running [FactorBase](https://github.com/sfu-cl-lab/FactorBase). If you use BIF_Generator after Factorbase, you can just keep the same configuration file.-->

4. Navigate to `BIF_Generator/jar` where BIF_Generator.jar is located. 
   
   Export the learned Bayesian Network (BN) by 
   
    `java -jar BIF_Generator.jar`.
   
   OR
   
   Navigate to parent directory `BIF_Generator` and compile the .java source code by 
   
    `javac -cp ".:./lib/*" BIF_Generator.java`  
    `java -cp ".:./lib/*" BIF_Generator`  
    
5. The output file is created in the folder `Bif_Generator` named `Bif_<YOURDATABASENAME>.xml`  

  
## Visualize the Bayesian Network  
We have tested the BIF_Generator with the AIspace tool from UBC.  
1. Download and run the tool

   [Download tool (.jar format)](http://www.aispace.org/bayes/version5.1.10/bayes.jar) and  
   Run by `java -jar bayes.jar`
  
    OR 
  
   [Download tool (.exe format)](http://www.aispace.org/bayes/version5.1.10/bayes.exe) and   
   Run the .exe file

2. Go to `File > Load from File` 
   and select the `Bif_<YOURDATABASENAME>.xml` in the folder `Bif_Generator`.

You will obtain the result shown in the Image ![BNinAIspace](/images/bnaispace.png).

  
<!---### Compile & Run (Alternative way to run BIF_Generator)    
+ Go into `cfg` folder and modify `subsetctcomputation.cfg` to make it identical to the config file you use to run FactorBase.    
+ `javac -cp ".:./lib/*" BIF_Generator.java`  
+ `java -cp ".:./lib/*" BIF_Generator`  -->
