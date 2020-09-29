
Import the SOAP xml project "CalculatorSOAPProject.xml" file
Also save the supported test data file "data.txt" and "testdata.xls" file to the same location where the xml is project is downloaded

Project has two TestSuites  
-CalculatorDataDrivenTestsuite
      Here Data driven testing  concept has been demonstrated with four different requests( Add,Divide,Multiply,Subtract) 
	  with three sets of data read from Excel file through Groovy Script testStep.
	  
	  And also data driven testing has been demonstrated using the CSV while which is also through Groovy Script test Step.
	  
	  For now only Script assertions are available in Add request.We can add similar assertions to all other requests in their corresponding test step.
	  
	  For Execution only one Groovy Script Test Steps invoke is enough to accomplish 12 tests.



-CalciMockTestSuite
    Dynamic mock service has been demonstrated in this suite
	
	Here I have created a AddMockSerive for Add request.
	The mock service has got three mock responses :
	Successful response is invoked when valid data is provided
	InvalidDataformat is invoked when invalid data is provided
	404 invoked for bad request

    In this test suite also the Groovy Script assertions (xsd validation) are provided for each Request test step.
	Dynamic mock responses get triggered with mapped header values in request.