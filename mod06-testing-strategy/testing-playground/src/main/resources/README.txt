┌───────────────────────────────────────────────────────────────────────────────────────┐
│ (\_/)          M U L E S O F T    T R A I N I N G   &   C E R T I F I C A T I O N     │
│ /   \          Anypoint Platform Architecture: Integration Solutions                  │
└───────────────────────────────────────────────────────────────────────────────────────┘

Application Name:
	testing-playground

Description:
	A set of simple and multiple route flows to explore MUnit test automation features

Usage Notes:
	The following are for local testing of the flows:
		http://localhost:8081/testing/helloPayload
		http://localhost:8081/testing/returnsAnError
		http://localhost:8081/testing/needsAStringAsAPayload
		http://localhost:8081/testing/scatterGather
		http://localhost:8081/testing/errorHandler
		http://localhost:8081/testing/choiceOf3Paths
			- body post/put can be hello, goodbye or any other value (set Content-Type header to text/plain)


Problems/Workarounds:
	Problem: Test coverage seems to only cover one test worth
	Solution: Make sure you are running all tests for the entire application 
	(right click on	the project name, go down to munit, run all tests to do this)

	Problem: Running tests with maven on command line fails
	Solution: Review the mule-artifact.json file is up to date with your version of mule
	runtime. This file takes priority when running with maven.

	Problem: Test Recorder fails to start on first run
	Solution: Restart the IDE and try again.

	Problem: Outbound calls fail for the flows using HTTP request
	Solution: If outbound communication requires a proxy - create a proxy configuration and then add to
	the two HTTP Request configurations in global.xml
	Alternative: Point the HTTP requests to the hello in the payload flow