# PerformanceTestTFL
### Introduction:

This document provides an overview of the Journey Planner script with the capability to search for different From and To stations using parameterization. 

### Test Scenario:

The objective of the test scenario is to validate the performance of the Journey Planner functionality of TFL web application by performing a search for different stations as inputs using parameterization.

### Testplan Creation:

I created a testplan called "TFL_PlanMYJourney.jmx" that contains two Threadgroups. The first Threadgroup, "TFL01_PlanMyJourney," is designed to test the "current time" functionality. It involves the following steps:

	> Launch the URL  
	> Click on the "PlanMyJourney" menu  
	> Search journey planner
  
The second Threadgroup, "TFL_02_Planmyjourney_FutureDate," is designed to test the "future time" functionality. It involves the following steps:

	> Launch the URL
	> Select a "FromStation"
	> Select a "ToStation"
	> Search journey planner for a future time

### Testplan Enhancement:

In order to enhance the testplan, I made the following changes:

For TFL01_PlanMyJourney with current time:

	> Parameterized the "FromStation" and "ToStation" fields with test data using a CSV file called "StationNames.csv" (change CSV file location under "TFL_01_PlanMyJourney_CurrentTime" to execute locally).
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

	> Execution 1: Test executed with embedded resources, results are attached with name "TFL_PlanMyJourney_TestReport_embeddedresource.xlsx". 
	> Execution 2: Test executed without embedded resources, results are attached with name "TFL_PlanMyJourney_TestReport.xlsx"
