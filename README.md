Run ```npm run cy:run:test1``` to run the example on 1 thread, and ```npm run cy:run:test``` to run it on 2.

2 threads : Total run time: 48.93s, executed in: 36.481, saved 12.449 (~25%)
1 thread  : Total run time: 44.53s, executed in: 58.024, saved -13.486 (~-30%)

Steps done by each command : 

* Clear the report folder
* Run the test with parallel. Sets the overwrite to false and json format to true. Sets the reporting tool to mochawesome.
* Merge reports with mochawesome-merge.
* Runs a custom aggregate script, to report test status at the top describe() section when you have multiple "child" describe.
* Build the report.