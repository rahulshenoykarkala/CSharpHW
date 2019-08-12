print "Hello World"
dir("${WORKSPACE}\\${repoName}"){	
	def msbuildBin = "C:\\Windows\\Microsoft.NET\\Framework\\v4.0.30319" 
 	def solutionFile = WORKSPACE + "\\archersearch\\Archer4.sln"     	def buildCmd = "MSBuild $solutionFile"
	retCode =  bat (script: "$buildCmd", returnStatus: true);
	if(retCode != 0){
		error("build failed");
	}
	else{
		print 'SUCCESSFUL'
	}
}
