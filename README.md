# PerformanceTestTFL
### Testplan Creation:

I created a testplan called "TFL_PlanMYJourney.jmx" that contains two Threadgroups. The first Threadgroup, "TFL01_PlanMyJourney," is designed to test the "current time" functionality. It involves the following steps:

	> Launching the URL  
	> Clicking on the "PlanMyJourney" menu  
	> Searching for a journey planner
  
The second Threadgroup, "TFL_02_Planmyjourney_FutureDate," is designed to test the "future time" functionality. It involves the following steps:

	> Launching the URL
	> Selecting a "FromStation" and "ToStation"  
	> Searching for a journey planner for a future time

### Testplan Enhancement:

In order to enhance the testplan, I made the following changes:

For TFL01_PlanMyJourney with current time:

	> Parameterized the "FromStation" and "ToStation" fields with test data using a CSV file called "StationNames.csv" (the CSV file location can be changed under "TFL_01_Planmyjourney_CurrentTime").
	> Added error handling for all transactions.
	> Added response assertions to ensure the correctness of the responses.

For TFL_02_Planmyjourney_FutureDate:

	> Used a "Json Extractor" to handle the "FromStation" and "ToStation" fields and demonstrated dynamic variable handling.  
	> Added error handling for all transactions.  
	> Added response assertions to ensure the correctness of the responses.

### Scenario Designing:

	> Each Threadgroup was assigned with 25 users, for a total of 50 users
	> Used "think time" concept to achieve the desired transactions

### Script Execution:

I executed the test plan twice. 

	> The first time, I executed the test with embedded resources and the results were attached with the name "TFL_PlanMyJourney_TestReport_embeddedresource.xlsx". 
	> The second time, I executed the test without embedded resources and the results were attached with the name "TFL_PlanMyJourney_TestReport.xlsx"
