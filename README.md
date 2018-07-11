# HelloWorld
This folder contains a test project with ruby gems with known vulnrabilities that have been patched and some that have not been patched.


*Dependency Check Scan Information*
  - For Ruby, Dependency Check uses 2 Analyzers, *Bundle Audit Analyzer* which scans the Gemfile.lock file in a given ruby project. 
  The Analyzer is just a wrapper for the ruby gem bundler-audit which does all the work for Dependency Check. This is why 
  Dependency Check only seems to scan in this case 3 Dependencies instead of all gems. It only formats the output from the 
  bundler-audit scan.
  - The other Analyzer Dependency Check uses for ruby projects is the *Ruby Gemspec Analyzer(Experimental Scan)* which scans the 
  Rakefile for a given Ruby project. This Analyzer though gives you all information about a given gem which after research 
  I have found has lead to a lot of false positives and duplicate information also given in Bundle Audit Analyzer. Due to this
  when running Bundle Audit Analyzer Dependency Check purposely disables the Ruby Gemspec Analyzer scan to only give you the 
  information you need.
  
