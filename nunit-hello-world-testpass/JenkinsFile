pipeline {
	agent any

	stages {
		stage('checkout'){
		    steps{
		        git 'https://github.com/agilas16/NUnitTestPass'
		    }
	    }
		stage('nunit_run'){
		    steps{
		        bat '"C:/Program Files (x86)/NUnit.org/nunit-console/nunit3-console.exe" nunit-hello-world-testpass/NUnitExamples.Tests/bin/Debug/NUnitExamples.Test.dll ';
    		}
		 }
		stage('nunit_testreport'){
		    steps{
		        nunit testResultsPattern: 'TestResult.xml'
		    }
		}
		     
    }
}
