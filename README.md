# BIF_Generator
[![Build Status](https://travis-ci.org/sfu-cl-lab/BIF_Generator.svg?branch=master)](https://travis-ci.org/sfu-cl-lab/BIF_Generator)       
BIF Generator for [FactorBase](https://github.com/sfu-cl-lab/FactorBase)   
##How to Use  
First you should import data into your database and run [FactorBase](https://github.com/sfu-cl-lab/FactorBase).    
###Run .jar    
+ In `jar` folder, create a config file `cfg/subsetctcomputation.cfg` with exactly same contents as the config file you use to run FactorBase.    
+ run `java -jar BIF_Generator.jar`  
+ The result will be generated as `Bif_YOURDATABASENAME.xml`     
  
###Compile & Run (Alternative way to run BIF_Generator)    
+ Go into `cfg` folder and modify `subsetctcomputation.cfg` to make it identical to the config file you use to run FactorBase.    
+ `javac -cp ".:./lib/*" BIF_Generator.java`  
+ `java -cp ".:./lib/*" BIF_Generator`  
  
###Show results in GUI    
You'll need a tool provided by UBC.   
[Download tool (.jar format)](http://www.aispace.org/bayes/version5.1.10/bayes.jar)    
[Download tool (.exe format)](http://www.aispace.org/bayes/version5.1.10/bayes.exe)    
  
